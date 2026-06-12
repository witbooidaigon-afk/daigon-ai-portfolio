# Architecture Gallery

Reference architectures for Daigon's flagship systems. Diagrams are simplified to communicate the design to a technical buyer; production builds include error handling, retries, logging, and credential management.

---

## Platform Overview

```
                         ┌──────────────────────────────┐
   Triggers              │     n8n (self-hosted VPS)     │            Channels
 ─────────────►          │   Orchestration + Logic       │          ──────────────►
 • Inbound call          │  webhooks · schedules · IF/   │   • SMS (Twilio)
 • Missed call           │  switch · code · retries      │   • WhatsApp (Meta)
 • Form / JotForm        │                               │   • Email (Gmail)
 • New Sheet row         │   ┌──────────┐  ┌──────────┐  │   • Slack / Telegram
 • WhatsApp message      │   │  AI LLMs │  │  Voice   │  │   • Voice (Retell/Vapi)
 • Webhook / Cal.com     │   │ GPT / Cl │  │ Retell/  │  │
 ─────────────►          │   │ aude     │  │ Vapi+11L │  │   Data: Sheets · Airtable
                         │   └──────────┘  └──────────┘  │         Notion · Postgres
                         └──────────────────────────────┘         Calendar: Cal.com
```

---

## 1. AI Voice Agent (Inbound/Outbound)

```
 Caller ─► Retell/Vapi (ASR: Whisper) ─► Custom LLM (GPT-4o + system prompt + KB)
        ─► Intent? ──► Book ─► Cal.com ─► Confirmation (SMS/WhatsApp)
                   └─► FAQ  ─► Knowledge base answer
                   └─► Escalate ─► Human notify (Slack) + call summary log
        ─► n8n webhook ─► CRM record (Sheets/Airtable) ─► Team notification
```

## 2. Missed-Call Text-Back & No-Show Recovery

```
 Missed call event ─► n8n ─► Twilio SMS "Sorry we missed you…" (within seconds)
                          ─► Slack alert to team
                          ─► Wait/branch ─► No reply? ─► follow-up sequence
 No-show (calendar) ─► n8n ─► recovery sequence (SMS/WhatsApp) ─► rebook link (Cal.com)
```
*Visual proof: live screenshots of this flow exist (missed-call flow, Slack alert, recovery stages).*

## 3. Speed-to-Lead

```
 New lead (form/ad/webhook/Sheet) ─► n8n ─► Enrich + Qualify (LLM)
   ─► Instant first-touch (SMS + WhatsApp + Email) within seconds
   ─► Hot? ─► route to team (Slack) + book (Cal.com)
   ─► CRM write (Sheets/Airtable) ─► follow-up sequence if no reply
```

## 4. Appointment Lifecycle (Cal.com)

```
 Request ─► Check availability ─► Book ─► Confirm
        ─► Reschedule/Cancel handlers (on request)
        ─► Reminder runner (scheduled) ─► SMS/WhatsApp/email
        ─► No-show ─► recovery (see #2)
```

## 5. Cold Outreach Engine

```
 Google Sheet (leads) ─► n8n sequencer ─► Personalise (LLM: name/industry/site)
   ─► Send (Gmail/SMS) with rate limits + business-hours guard
   ─► IMAP/inbox watch ─► Reply detected? ─► STOP follow-ups + route to human
   ─► Update status in Sheet (sent / replied / do-not-contact)
```

## 6. CRM & Lifecycle (Spa template)

```
 Lead ─► Book (Cal.com) ─► Retell handler (voice) ─► Reminders (runner)
      ─► Post-visit follow-up ─► Review request ─► Re-engagement/upsell
      ─► All states logged in Sheets (CRM template)
```

---

## Existing Visual Assets (Inventory)

| Asset | Location | Use |
|---|---|---|
| Missed-call & no-show flow screenshots (7+ images) | `AI-Workflows/Missed-Call/` | Case Study 3 proof |
| Slack alert screenshot | `AI-Workflows/Missed-Call/` | Notification proof |
| Workflow build docs (Markdown) | `Lead-Systems/`, `Assistants/` | Architecture/setup reference |
| Retell agent config & system-prompt docs | `Assistants/` | Voice-agent design reference |
| Agency pricing decks, pitch deck, service guides | `AGENCY/Dynamic-Media/` | Sales collateral |

## Asset Gaps (to strengthen this gallery)

- Exported visual diagrams of each flagship flow (rendered, not ASCII).
- A 60–90s screen-recording of a live workflow executing (any system).
- Before/after metrics for one deployment (response time, recovered calls).

*(Full collection plan in `Portfolio.md` → Asset Checklist.)*
