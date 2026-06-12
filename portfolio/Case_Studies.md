# Case Studies

Selected deployments illustrating how Daigon turns a business problem into a working AI system. Each study lists a **Confidence Level** reflecting how much hard proof (live workflow files, screenshots, multiple iterations) currently backs it — an honesty signal for both us and the client.

> **Confidence:** ⭐⭐⭐ Strong (working files + screenshots/iterations) · ⭐⭐ Solid (working files) · ⭐ Demo/prototype

---

## Case Study 1 — Day-Spa CRM & Lifecycle Automation  ⭐⭐⭐
**Sector:** Health & wellness (spa)

- **Problem:** A spa was managing bookings, reminders, and follow-ups manually, losing time and repeat business.
- **Solution:** A three-workflow CRM covering the full customer lifecycle — Cal.com booking lifecycle, a Retell voice handler, and a reminder runner.
- **Architecture:** n8n orchestration → Cal.com (events) → Retell (voice) → Google Sheets (records) → messaging (reminders/follow-ups).
- **Technology stack:** n8n, Cal.com, Retell AI, Google Sheets, GPT-4o, Twilio/WhatsApp.
- **Business impact:** Automated booking, reminders, and review/follow-up flows; reduced no-shows and admin load; more repeat visits.
- **Automation benefits:** Runs 24/7; no manual reminder texts; consistent post-visit follow-up.
- **Scalability:** Template re-deployable to any appointment-based wellness business.
- **Future improvements:** Add upsell/membership nurture and a live dashboard.
- **Visual assets available:** Workflow files (3 iterations) + CRM sheet template.

## Case Study 2 — Plumbing Outbound Voice Agent  ⭐⭐⭐
**Sector:** Home services (plumbing)

- **Problem:** Outbound calling and lead qualification didn't scale, and after-hours calls were missed.
- **Solution:** A Retell custom-LLM voice agent that calls/answers, qualifies, and books — iterated across multiple versions (v9 and patched releases).
- **Architecture:** Retell AI (custom LLM) → n8n webhook handler → call-analysis branch → booking section → CRM/notification.
- **Technology stack:** Retell AI, custom LLM endpoint, n8n, Cal.com, GPT-4o.
- **Business impact:** Scales calling capacity without added headcount; captures and books leads conversationally.
- **Automation benefits:** Consistent qualification, automatic booking, full call logging.
- **Scalability:** Swap the knowledge base and number to deploy for any trade.
- **Future improvements:** Add call-recording analytics and outcome dashboards.
- **Visual assets available:** Multiple workflow iterations + agent config docs.

## Case Study 3 — Missed-Call Text-Back & No-Show Recovery  ⭐⭐⭐
**Sector:** Cross-industry (appointment-based businesses)

- **Problem:** Missed calls and no-shows were silent, recurring revenue leaks.
- **Solution:** Instant SMS text-back on every missed call, plus automated no-show recovery sequences with team alerts.
- **Architecture:** Telephony event → n8n → Twilio (SMS) → Slack alert → recovery sequence.
- **Technology stack:** n8n, Twilio, Slack, calendar integration.
- **Business impact:** Recovers conversations and rebookings that would otherwise be lost entirely.
- **Automation benefits:** Near-zero effort, fastest ROI to demonstrate.
- **Scalability:** Drop-in for any business with a phone number and a calendar.
- **Future improvements:** Add conversion tracking to quantify recovered revenue.
- **Visual assets available:** ⭐ **Screenshots of live flows** (missed-call flow, Slack alerts, no-show recovery stages) — strongest visual proof in the portfolio.

## Case Study 4 — HVAC / Home-Services Cold Outreach Engine  ⭐⭐⭐
**Sector:** HVAC & home services

- **Problem:** Inconsistent outbound prospecting limited pipeline growth.
- **Solution:** A scalable cold-outreach engine, iterated across HVAC v1–v3 and a parallel agency build (DMA v4–v7), with personalised messaging, safe sending, and reply detection.
- **Architecture:** Google Sheets (lead list) → n8n sequencer → personalised generation → Gmail/SMS → reply detection → auto-stop & routing.
- **Technology stack:** n8n, Google Sheets, Gmail, GPT-4o-mini, messaging.
- **Business impact:** Reliable top-of-funnel without a manual SDR; reps handle only warm replies.
- **Automation benefits:** Rate-limited safe sending, personalisation at scale, automatic follow-up cessation on reply.
- **Scalability:** Re-pointed to any vertical's lead list and offer.
- **Future improvements:** A/B subject testing and deliverability monitoring.
- **Visual assets available:** Multiple workflow versions + a library of 50 outreach scripts.

## Case Study 5 — Family-Law Inbound AI Agent  ⭐⭐
**Sector:** Legal services

- **Problem:** Inbound enquiries needed fast, consistent intake and routing.
- **Solution:** An inbound AI agent that greets, gathers case basics, and routes/booked qualified enquiries.
- **Architecture:** Inbound channel → n8n → AI intake agent → routing/booking → notification.
- **Technology stack:** n8n, GPT-4o, Cal.com, messaging.
- **Business impact:** Faster intake, consistent qualification, fewer missed enquiries.
- **Scalability:** Adaptable to any professional-services intake.
- **Future improvements:** Add conflict-check prompts and CRM sync.
- **Visual assets available:** Workflow files (two iterations).

## Case Study 6 — Fitness Growth Engine  ⭐⭐
**Sector:** Fitness / gyms

- **Problem:** Member acquisition and follow-up were manual and inconsistent.
- **Solution:** A vertical "growth engine" template combining lead capture, instant response, and nurture.
- **Architecture:** Lead capture → n8n → qualification → multi-channel nurture → booking.
- **Technology stack:** n8n, GPT-4o, Sheets/Airtable, WhatsApp/SMS/email.
- **Business impact:** Faster lead handling and consistent nurture for trials/sign-ups.
- **Scalability:** Vertical template re-deployable across fitness businesses.
- **Future improvements:** Add retention/win-back sequences.
- **Visual assets available:** Workflow file.

---

## Additional Engagements (Brief)

- **Pet-care support agent** (Bow Wow) — knowledge-grounded customer-support agent. ⭐
- **Client brand & systems engagements** — Grace Community Church, Ahren, Booty.Fun (delivery/brand work; light detail).

---

### Note on Confidence Levels
Confidence reflects available *proof artifacts*, not the quality of the build. Several ⭐⭐ studies become ⭐⭐⭐ with one screen-recording or before/after metric — see the **Asset Checklist** in `Portfolio.md`.
