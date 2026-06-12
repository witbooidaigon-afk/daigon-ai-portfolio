# Build Showcase — Working Demos & Proof-of-Concepts

> **What this is — read first.** These are AI systems I **designed, built, and tested**, and **demoed to prospects**. They are *not* paid client case studies — I didn't land paying clients from these specific builds. They are real, working systems I created to learn, to prove a concept, and to show what's possible. Everything below describes what each build **does and is designed to deliver** — validated in my own testing, not audited client results.

> **Proof level:** ⭐⭐⭐ Strong (working files + screenshots/iterations) · ⭐⭐ Solid (working files) · ⭐ Early demo/prototype

---

## Build 1 — Day-Spa CRM & Lifecycle Automation  ⭐⭐⭐
**Built for:** Health & wellness (spa) use case

- **Problem it tackles:** A spa managing bookings, reminders, and follow-ups manually loses time and repeat business.
- **What I built:** A three-workflow CRM covering the full customer lifecycle — Cal.com booking lifecycle, a Retell voice handler, and a reminder runner.
- **Architecture:** n8n orchestration → Cal.com (events) → Retell (voice) → Google Sheets (records) → messaging (reminders/follow-ups).
- **Technology:** n8n, Cal.com, Retell AI, Google Sheets, GPT-4o, Twilio/WhatsApp.
- **What it's built to do:** Automate booking, reminders, and post-visit follow-up; reduce no-shows and admin load; encourage repeat visits.
- **Reusability:** Template re-deployable to any appointment-based wellness business.
- **Proof available:** Working workflow files (3 iterations) + a CRM sheet template.

## Build 2 — Plumbing Outbound Voice Agent  ⭐⭐⭐
**Built for:** Home services (plumbing) use case

- **Problem it tackles:** Outbound calling and lead qualification don't scale, and after-hours calls get missed.
- **What I built:** A Retell custom-LLM voice agent that calls/answers, qualifies, and books — iterated across multiple versions (v9 and patched releases).
- **Architecture:** Retell AI (custom LLM) → n8n webhook handler → call-analysis branch → booking section → record/notification.
- **Technology:** Retell AI, custom LLM endpoint, n8n, Cal.com, GPT-4o.
- **What it's built to do:** Scale calling capacity conversationally without added headcount; qualify and book leads; log calls.
- **Reusability:** Swap the knowledge base and number to adapt for any trade.
- **Proof available:** Multiple working workflow iterations + agent config docs.

## Build 3 — Missed-Call Text-Back & No-Show Recovery  ⭐⭐⭐
**Built for:** Cross-industry (any appointment-based business)

- **Problem it tackles:** Missed calls and no-shows are silent, recurring revenue leaks.
- **What I built:** Instant SMS text-back on every missed call, plus automated no-show recovery sequences with team alerts.
- **Architecture:** Telephony event → n8n → Twilio (SMS) → Slack alert → recovery sequence.
- **Technology:** n8n, Twilio, Slack, calendar integration.
- **What it's built to do:** Re-engage missed callers and no-shows automatically, with near-zero effort.
- **Reusability:** Drop-in for any business with a phone number and a calendar.
- **Proof available:** ⭐ **Screenshots of the live flows** (missed-call flow, Slack alerts, no-show recovery stages) — the strongest visual proof in this showcase.

## Build 4 — HVAC / Home-Services Cold Outreach Engine  ⭐⭐⭐
**Built for:** HVAC & home services use case

- **Problem it tackles:** Inconsistent outbound prospecting limits pipeline growth.
- **What I built:** A scalable cold-outreach engine, iterated across HVAC v1–v3 and a parallel agency build (v4–v7), with personalised messaging, safe sending, and reply detection.
- **Architecture:** Google Sheets (lead list) → n8n sequencer → personalised generation → Gmail/SMS → reply detection → auto-stop & routing.
- **Technology:** n8n, Google Sheets, Gmail, GPT-4o-mini, messaging.
- **What it's built to do:** Run reliable, rate-limited outbound prospecting at scale without a manual SDR; stop follow-ups automatically on reply.
- **Reusability:** Re-point to any vertical's lead list and offer.
- **Proof available:** Multiple working workflow versions + a library of 50 outreach scripts.

## Build 5 — Family-Law Inbound AI Agent  ⭐⭐
**Built for:** Legal services use case

- **Problem it tackles:** Inbound enquiries need fast, consistent intake and routing.
- **What I built:** An inbound AI agent that greets, gathers case basics, and routes/books qualified enquiries.
- **Architecture:** Inbound channel → n8n → AI intake agent → routing/booking → notification.
- **Technology:** n8n, GPT-4o, Cal.com, messaging.
- **What it's built to do:** Speed up intake, qualify consistently, and reduce missed enquiries.
- **Reusability:** Adaptable to any professional-services intake.
- **Proof available:** Working workflow files (two iterations).

## Build 6 — Fitness Growth Engine  ⭐⭐
**Built for:** Fitness / gym use case

- **Problem it tackles:** Member acquisition and follow-up are manual and inconsistent.
- **What I built:** A vertical "growth engine" template combining lead capture, instant response, and nurture.
- **Architecture:** Lead capture → n8n → qualification → multi-channel nurture → booking.
- **Technology:** n8n, GPT-4o, Sheets/Airtable, WhatsApp/SMS/email.
- **What it's built to do:** Handle leads faster and nurture trials/sign-ups consistently.
- **Reusability:** Vertical template re-deployable across fitness businesses.
- **Proof available:** Working workflow file.

---

## Other Builds (Brief)

- **Pet-care support agent** (Bow Wow) — a knowledge-grounded customer-support agent. ⭐ early demo.
- **BntyFul — Business Indexing & Influencer Intelligence Pipeline** — my most advanced self-built system (a multi-layer, prompt-centric research/indexing pipeline). See the AI Engineer Profile for the full write-up.

---

### Note on proof levels
Proof reflects available *artifacts* (working files, screenshots, iterations), not paid outcomes. Several ⭐⭐ builds become ⭐⭐⭐ with one short screen-recording — see the Asset Checklist in `Portfolio.md`.
