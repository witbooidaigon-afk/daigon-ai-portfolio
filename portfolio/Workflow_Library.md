# Workflow Library

A catalogued, de-duplicated index of Daigon's production automation systems. Multiple iterations of the same system (e.g. outreach v4–v7) are grouped into a single product entry. Each entry is a **reusable system** that can be re-deployed to a new client.

> **Status legend:** ✅ Deployed / proven · 🧪 Built & tested · 🔧 In active iteration

---

## 1. AI Voice Agent (Inbound & Outbound) — ✅
**Source:** `Plumber-Outreach-Agent/`, `Retell-WhatsApp/`, `Misc/Inbound Agent For Amplify Family Law`
- **Triggers:** Inbound phone call, outbound call list, or webhook
- **AI components:** Retell AI / Vapi custom-LLM, GPT-4o reasoning, ElevenLabs voice, Whisper transcription
- **Actions:** Greets caller, qualifies intent, answers FAQs from business knowledge, books or routes the call, logs outcome, notifies team
- **Inputs:** Caller audio, business knowledge base, calendar availability
- **Outputs:** Booked appointment, qualified lead record, call summary, team notification
- **Time saved:** Replaces/extends a front-desk receptionist; captures after-hours calls that would otherwise be lost

## 2. Appointment Booking System — ✅
**Source:** `AI-Workflows/Appointment-Booking/` (check-availability, book, reschedule, cancel, reminders, Cal.com event router)
- **Triggers:** Booking request (chat/voice/form), Cal.com event, schedule
- **AI components:** Conversational agent for natural-language booking
- **Actions:** Checks availability → books → reschedules/cancels on request → sends reminders → recovers no-shows
- **Integrations:** Cal.com, Google Calendar, WhatsApp/SMS/email
- **Outputs:** Confirmed bookings, reminder sequences, reduced no-shows
- **Time saved:** Eliminates back-and-forth scheduling and manual reminders

## 3. Speed-to-Lead System — ✅
**Source:** `AI-Workflows/Lead-Systems/` (Speed to Lead System, Lead Intelligence Engine build docs)
- **Triggers:** New lead (form, ad, webhook, new sheet row)
- **AI components:** Lead enrichment & qualification, personalised first-touch message generation
- **Actions:** Instantly contacts the lead via SMS/WhatsApp/email, qualifies, routes hot leads to the team
- **Outputs:** Sub-minute first response, qualified & routed lead, CRM record
- **Time saved:** Cuts response time from hours to seconds — the single biggest driver of lead conversion

## 4. Missed-Call Text-Back & No-Show Recovery — ✅
**Source:** `AI-Workflows/Missed-Call/` (missed_call_sms_textback, missed_call_textback, no-show recovery — **with screenshots**)
- **Triggers:** Missed inbound call; no-show flagged in calendar
- **AI components:** Context-aware re-engagement messaging
- **Actions:** Auto-texts the missed caller within seconds; runs no-show recovery sequences; alerts team via Slack
- **Integrations:** Twilio, Slack, calendar
- **Outputs:** Recovered conversation, re-booked appointment, team alert
- **Time saved / value:** Recovers revenue from calls that would otherwise be lost entirely — *highest-ROI, lowest-effort install*

## 5. Cold Outreach Engine — ✅
**Source:** `AI-Workflows/Outreach/` (DMA v4–v7 scalable, HVAC v1–v3), plus 50 cold-outreach scripts
- **Triggers:** Lead list (Google Sheets), schedule
- **AI components:** Personalised message generation per lead (business name, industry, website context)
- **Actions:** Multi-step sequencing, safe-send rate limiting, reply detection that auto-stops follow-ups
- **Integrations:** Google Sheets, Gmail, WhatsApp/SMS
- **Outputs:** Booked calls/replies, clean pipeline, do-not-contact handling
- **Time saved:** Runs outbound prospecting at scale without a manual SDR

## 6. WhatsApp AI Agent — ✅
**Source:** `AI-Workflows/WhatsApp/`, `Retell-WhatsApp/whatsapp-dyna-workflow`
- **Triggers:** Inbound WhatsApp message
- **AI components:** Conversational agent grounded in business knowledge
- **Actions:** Answers questions, qualifies, books, escalates to human when needed
- **Integrations:** WhatsApp Business API (Meta Graph), Cal.com, Sheets/Airtable
- **Outputs:** 24/7 conversational sales/support on the channel customers actually use

## 7. AI Customer-Support Agent — 🧪
**Source:** `Misc/Bow Wow Support Agent`, support-agent configs
- **Triggers:** Inbound support message (web/WhatsApp)
- **AI components:** Knowledge-grounded support agent
- **Actions:** Resolves common queries, looks up order/booking info, escalates edge cases, logs tickets
- **Outputs:** Deflected support volume, faster resolution

## 8. CRM & Customer-Lifecycle Automation — ✅
**Source:** `AI-Workflows/Bliss-Spa-CRM/` (Cal.com lifecycle, Retell handler, reminder runner)
- **Triggers:** New customer, booking event, lifecycle stage change
- **AI components:** Conversational handlers + lifecycle logic
- **Actions:** Captures lead → books → reminds → follows up → requests review → re-engages
- **Integrations:** Cal.com, Retell, Sheets, messaging
- **Outputs:** End-to-end automated customer journey, higher retention & repeat bookings

## 9. AI Back-Office Assistant Pack — ✅
**Source:** `AI-Workflows/Assistants/` (Email Agent, Follow-up Agent, Review Request Agent, Daily Assistant, Proposal/Quote automation)
- **Email Agent:** Triages, drafts, and sends email
- **Follow-up Agent:** Chases unanswered threads automatically
- **Review Request Agent:** Requests Google reviews after a job
- **Proposal/Quote Automation:** Generates and sends proposals/quotes from structured inputs
- **Daily Assistant:** Daily briefings, reminders, and task prep
- **Outputs:** Hours of admin time removed per week per business

## 10. Industry Growth Engines (Vertical Templates) — 🔧
**Source:** `Misc/kfit-ai-growth-engine`, HVAC/solar variants, vertical-specific builds
- Pre-tuned versions of the systems above for specific industries (fitness, HVAC, solar/energy, home services, legal, pet care)
- **Value:** Faster deployment and instantly relevant messaging per vertical

---

## Library Summary

| # | System | Status | Primary Value |
|---|---|---|---|
| 1 | AI Voice Agent | ✅ | Never miss a call |
| 2 | Appointment Booking | ✅ | Zero-admin scheduling |
| 3 | Speed-to-Lead | ✅ | Seconds-fast lead response |
| 4 | Missed-Call / No-Show Recovery | ✅ | Recover lost revenue |
| 5 | Cold Outreach Engine | ✅ | Outbound at scale |
| 6 | WhatsApp AI Agent | ✅ | 24/7 chat sales/support |
| 7 | AI Support Agent | 🧪 | Deflect support load |
| 8 | CRM / Lifecycle Automation | ✅ | Full journey on autopilot |
| 9 | Back-Office Assistant Pack | ✅ | Remove admin hours |
| 10 | Industry Growth Engines | 🔧 | Vertical fast-deploy |
