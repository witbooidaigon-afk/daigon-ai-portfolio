# AI Engineer Profile

**Name:** _[add your name]_
**Brand:** Daigon · Dynamic Media
**Role:** AI Automation & Voice-Agent Engineer
**Location:** South Africa
**Email:** dynamicmediaagency2025@gmail.com

*A personal, first-person profile of how I think, build, and work with AI systems. Honest about what I've shipped and where I'm still growing.*

---

## 01 · Introduction

I'm a self-taught AI automation engineer, and I'm at my best when I'm building. Give me a messy, manual business process and I'll turn it into a workflow that just runs — removing the busywork and making things faster. I learn a tool by building something real with it, breaking it, refining it, and keeping what works.

My focus is **applied AI** — connecting today's best models to real workflows, rather than research or model training. So far I've built 40+ automation systems: AI voice agents, lead and missed-call recovery, appointment booking, outreach engines, and an AI research & indexing pipeline — each one **built, tested, and demoed to prospects**. Some started as client work; others I built purely to learn or to prove an idea. I care about systems that are reliable, reusable, and genuinely useful — not clever for its own sake.

## 02 · Technical Profile

- **Primary discipline:** Workflow automation engineering with n8n, plus AI agent and voice-agent development.
- **AI fluency:** Comfortable orchestrating multiple LLM providers (OpenAI, Anthropic) and matching the right model to each task.
- **Integration depth:** I connect telephony, messaging, calendars, spreadsheets, CRMs, and webhooks into single coherent systems.
- **Delivery style:** Iterative — I version workflows aggressively (v1 → v7), test against real inputs, and harden for reliability.
- **Self-hosting:** I run my own n8n instance on a VPS rather than relying on managed automation SaaS.
- **AI-assisted development:** I build fast using Claude Code and Cursor as part of my daily process.

## 03 · Core Competencies

- AI agent design (chat, messaging, and voice)
- n8n workflow engineering (webhooks, branching, retries, scheduling)
- Voice AI (inbound & outbound phone agents)
- Multi-channel messaging automation (SMS, WhatsApp, email, Slack, Telegram)
- Lead and customer-lifecycle automation (capture → qualify → book → follow-up)
- Systems integration across APIs and webhooks
- Prompt engineering and agent guardrails
- Knowledge-grounded agents (business-specific Q&A)
- Data routing across Sheets, Airtable, Notion, and Postgres
- Rapid prototyping with AI coding tools

## 04 · AI Engineering Stack

- **LLMs:** OpenAI GPT-4o / 4o-mini / 4.1 / 5 · Anthropic Claude Sonnet 4
- **Speech:** Whisper (speech-to-text) · ElevenLabs (text-to-speech)
- **Voice agents:** Retell AI (custom-LLM) · Vapi
- **Model strategy:** small/cheap models for classification and drafting; frontier models for reasoning and complex conversation — chosen per task to balance cost and quality.

I treat models as interchangeable components and design so I can swap them as better/cheaper options appear.

## 05 · Workflow Engineering Methodology

My workflow builds follow a consistent loop:

1. **Map the business process** — what happens today, manually, and where it breaks.
2. **Define triggers, inputs, and outputs** before touching nodes.
3. **Build the happy path first**, then add branching for edge cases.
4. **Iterate in versions** — I keep numbered versions (e.g. v4 → v7) so I can compare and roll back. My outreach and voice builds went through many iterations before they were dependable.
5. **Harden for reliability** — add retries, error handling, rate limiting, and safe-sending guards.
6. **Document the build** so it can be re-deployed to a new client or context quickly.

The result is a library of **productized, reusable systems** rather than one-off scripts.

## 06 · Automation Architecture

I standardise on **n8n, self-hosted on a Hostinger VPS**, as my orchestration core. A typical system looks like:

```
Trigger (call / missed call / form / new row / WhatsApp / webhook / schedule)
   → n8n (logic, branching, retries, code nodes)
       → AI layer (LLM reasoning, voice, transcription)
       → Channels (SMS, WhatsApp, email, Slack)
       → Data (Sheets / Airtable / Notion / Postgres) + Calendar (Cal.com)
```

I prefer self-hosting for control, data ownership, and cost — and I lean on managed APIs (OpenAI, Anthropic, Retell, Twilio, Cal.com) where managed services clearly win.

## 07 · AI Systems Built

Real systems I've designed, built, and tested — and demoed to prospects. Some began as client work; others I built to learn or prove an idea:

- **BntyFul — Business Indexing & Influencer Intelligence Pipeline** *(self-built; my most advanced system)* — an AI research pipeline that discovers, vets, scores, and **indexes influencers/creators for a given brand**. A "Master Orchestrator" (n8n + a `DAIGON CRM` Google Sheet of executable prompts) dispatches per-category research jobs to a **cloud agent** that drives a **browser via Playwright** to run AI research against embedded reference documents, then returns **scored reports, opportunity lists, and lead-quality analysis** into per-brand master pipelines (with ICP definitions, scoring cards, and ignore lists). I evolved the architecture across **three versions (V1 → V2 → V3)**, landing on a **prompt-centric design** where a single "executable prompt" carries the instructions, references, and routing — with **async webhook callbacks, run-ID tracking, and error logging**. Applied to multiple brand pipelines (e.g. a sports/"Rivals" category and several consumer brands), plus a supporting SA influencer-events intelligence database.
- **AI Voice Agents** — inbound/outbound phone agents that qualify callers and book jobs (built and iterated for a plumbing use case and a family-law inbound agent).
- **Missed-Call Text-Back & No-Show Recovery** — instant SMS text-back and automated recovery sequences (I have working flows and screenshots of these).
- **Speed-to-Lead** — sub-minute first response to new leads across SMS/WhatsApp/email.
- **Appointment Booking** — Cal.com booking, rescheduling, cancellation, and reminders.
- **Cold Outreach Engines** — personalised, rate-limited outreach with reply detection (HVAC and agency versions, many iterations).
- **WhatsApp AI Agents** — knowledge-grounded conversational agents.
- **Spa CRM & Lifecycle** — a three-workflow customer-lifecycle system (booking → reminders → follow-up).
- **Back-Office Assistants** — email triage, follow-up chasing, proposal/quote generation, review requests.
- **Customer-Support Agent** — a knowledge-grounded support agent (pet-care prototype).

I'm honest about status: these are working builds I've tested and shown to prospects — some ran in real client contexts, others I built to learn or prove an idea. I mark them honestly rather than overclaim.

**What building BntyFul taught me.** This was the project where I grew the most as an engineer. I learned to design **multi-layer systems** (CRM → orchestrator → cloud agent → browser execution → AI processing → results), to keep an orchestrator **thin** and push intelligence into portable, versioned "executable prompts," and to handle **asynchronous execution** properly — immediate acknowledgements, callbacks, timeouts, run tracking, and error workflows instead of brittle one-shot scripts. The biggest realization was that, in this design, **prompt engineering becomes systems engineering**: a single badly-structured prompt can misroute logic or break a run, so I now treat prompts as critical infrastructure with strict templates (`[ROLE] [TASK] [REFERENCES] [EXECUTION RULES] [OUTPUT FORMAT] [FAIL CONDITIONS]`), predictable reference standards, and version history. It also pushed me into **browser automation** (Playwright with abstracted actions) and building a real **research/scoring/indexing data pipeline** with ICPs and ignore lists.

## 08 · Knowledge Systems & RAG

I build **knowledge-grounded agents** so responses are accurate to a specific business — services, pricing, FAQs, policies — rather than generic. Today I mostly achieve this through structured system prompts and curated knowledge sources (Notion, Sheets, and documents) fed into the agent's context.

**Where I'm growing:** moving toward formal retrieval-augmented generation (vector search over larger document sets) for businesses with bigger knowledge bases. This is a deliberate next step in my skill development, not something I overstate today.

## 09 · Voice AI Experience

Voice is one of my strongest and most-practised areas:

- **Platforms:** Retell AI (including custom-LLM configuration) and Vapi.
- **Components:** Whisper for transcription, ElevenLabs for natural voice, GPT-4o for reasoning, Cal.com for booking.
- **What I've built:** outbound and inbound agents that greet, qualify, answer questions from a knowledge base, book appointments, escalate to a human when needed, and log call summaries.
- **Iteration:** my plumbing voice agent went through many versions (including patched releases) to get conversation flow and booking reliable.

## 10 · Personal Workflow Library

Over time I've built a personal, reusable library of 40+ workflows, grouped by product: voice agents, speed-to-lead, missed-call recovery, appointment booking, outreach engines, WhatsApp agents, CRM/lifecycle, and back-office assistants — plus vertical "growth engine" templates tuned for specific industries. Because they're templated and documented, I can re-deploy a system to a new context in days rather than rebuilding from scratch.

## 11 · Development Process

- **AI-first building:** I use **Claude Code** and **Cursor** daily to design, build, and debug faster.
- **Iterative and test-driven in spirit:** build small, test against real inputs, refine, version.
- **Reuse over reinvention:** I start from my own templates and proven patterns.
- **Documentation alongside builds:** I write setup/build guides so systems are maintainable and transferable.
- **Pragmatic:** I optimise for reliability and business outcome, not cleverness.

## 12 · Tooling & Infrastructure

- **Automation:** n8n (self-hosted on Hostinger VPS)
- **AI build tools:** Claude Code, Cursor, VS Code
- **Version control:** Git / GitHub
- **Design:** Figma
- **Comms & data:** Google Workspace (Sheets, Gmail, Docs, Calendar), Airtable, Notion, Slack, Telegram
- **Telephony/voice:** Retell, Vapi, Twilio, ElevenLabs, WhatsApp Business API
- **Scheduling:** Cal.com
- **Browser automation:** Playwright (cloud-agent / AI-research execution)
- **Languages:** Python (scripting/data), JavaScript (n8n code nodes)

## 13 · Learning & Research Process

I learn by doing, supported by deliberate research:

- I collect and work through build guides and references (n8n chatbot guides, Notion + AI guides, Retell agent configuration docs, outreach playbooks) and then implement them hands-on.
- I use AI assistants (Claude, ChatGPT) as research and pair-building partners to accelerate understanding.
- I iterate in public-of-one: build a version, see where it fails, research the gap, rebuild.
- I keep a personal archive of scripts, configs, and templates so each project compounds into the next.

This loop — research → build → break → refine → template — is how I've gone from individual workflows to a coherent system library.

## 14 · Current AI Stack Costs (my own tooling)

*Estimates of what I spend to run my own development stack — usage-based items scale with how much I'm building/running. Not client pricing.*

- **VPS (n8n hosting):** ~$15–$40/mo
- **OpenAI API:** ~$20–$150/mo (usage-based)
- **Anthropic Claude / Claude Code:** ~$20–$200/mo
- **Retell AI / Vapi (voice):** ~$30–$200/mo when running voice agents
- **Twilio (SMS/voice):** ~$20–$150/mo (usage-based)
- **ElevenLabs:** ~$5–$99/mo
- **Cal.com / Google Workspace / Airtable / Notion:** ~$10–$70/mo combined
- **Cursor / Figma / GitHub:** ~$0–$55/mo

**Typical personal baseline:** roughly **$90–$250/mo** in fixed tooling, rising with active client/voice usage. I deliberately keep the fixed base low by self-hosting n8n.

## 15 · Future Direction

Where I'm taking my skills next:

- **Formal RAG & knowledge bases** — vector search over larger document sets for richer, more accurate agents.
- **Multi-agent systems** — coordinated agents (sales + support + ops) that share context.
- **Analytics dashboards** — live reporting on what my systems actually produce (leads recovered, response times, bookings).
- **Document processing & OCR** — automated invoice/quote/intake extraction.
- **Deeper engineering fundamentals** — stronger testing, version control discipline, and packaging my workflow library into proper repositories.
- **Productizing & white-labelling** — turning my best systems into templates other operators can deploy.

---

*This profile is an honest snapshot of my current capabilities and trajectory as an AI automation and voice-agent engineer. I'm comfortable saying what I've shipped, what's still a prototype, and what I'm actively learning.*
