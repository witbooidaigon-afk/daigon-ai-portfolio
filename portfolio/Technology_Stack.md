# Technology Stack Inventory

A complete inventory of the tools, models, and platforms Daigon uses in production. Items marked *(evidence-based)* were confirmed directly from live workflow files; others are part of the standard delivery toolkit.

---

## AI Models & Intelligence

| Tool | Role | Notes |
|---|---|---|
| **OpenAI GPT-4o / GPT-4o-mini** | Primary reasoning & chat for agents | Most-used model across workflows *(evidence-based)* |
| **OpenAI GPT-4.1 / 4.1-mini / 4.1-nano** | Cost-tuned task models | Used for lightweight classification/drafting *(evidence-based)* |
| **OpenAI GPT-5 / GPT-5-chat** | Highest-capability tasks | *(evidence-based)* |
| **Anthropic Claude Sonnet 4** | Reasoning, long-context, drafting | `claude-sonnet-4` referenced in workflows *(evidence-based)* |
| **OpenAI Whisper** | Speech-to-text transcription | Voice & call handling *(evidence-based)* |
| **ElevenLabs** | Natural AI voice (TTS) | Voice-agent output *(evidence-based)* |

## Voice & Telephony

| Tool | Role |
|---|---|
| **Retell AI** | Inbound/outbound AI voice agents (custom-LLM) — `api.retellai.com` *(evidence-based)* |
| **Vapi** | Alternative voice-agent runtime *(evidence-based)* |
| **Twilio** | SMS & voice transport (missed-call text-back, reminders) *(evidence-based)* |

## Automation Platform

| Tool | Role |
|---|---|
| **n8n (self-hosted)** | Core workflow orchestration engine, running on a dedicated Hostinger VPS *(evidence-based)* |
| Webhooks / HTTP Request | Custom integration glue *(evidence-based)* |
| Schedule / Cron triggers | Time-based automations (reminders, runners) *(evidence-based)* |

> **Note:** Make.com is **not** part of our stack. We standardise on n8n for control, self-hosting, and cost.

## Communication Channels

| Tool | Role |
|---|---|
| **WhatsApp Business API** (Meta Graph) | Conversational agents & notifications *(evidence-based)* |
| **Gmail / Google Mail** | Email send, triage, follow-up *(evidence-based)* |
| **Telegram** | Notifications & lightweight bots *(evidence-based)* |
| **Slack** | Internal team alerts (new lead, missed call) *(evidence-based)* |

## Scheduling & Calendars

| Tool | Role |
|---|---|
| **Cal.com** | Booking, rescheduling, cancellation, event routing *(evidence-based)* |
| **Google Calendar** | Calendar sync & availability *(evidence-based)* |

## Data, CRM & Storage

| Tool | Role |
|---|---|
| **Google Sheets** | Primary lead/customer source-of-truth in many builds *(evidence-based)* |
| **Airtable** | Structured CRM / pipeline data *(evidence-based)* |
| **Notion** | Knowledge base & content ops *(evidence-based)* |
| **Postgres** | Relational data store for select builds *(evidence-based)* |
| **Salesforce** | Enterprise CRM integration (where required) *(evidence-based)* |
| **Google Docs** | Document generation/output *(evidence-based)* |

## Forms & Capture

| Tool | Role |
|---|---|
| **JotForm** | Lead capture forms *(evidence-based)* |
| **n8n Form Trigger** | Native intake forms *(evidence-based)* |

## Developer & Design Tooling

| Tool | Role |
|---|---|
| **GitHub** | Version control |
| **VS Code** | Primary editor |
| **Claude Code** | AI pair-engineering & build automation |
| **Cursor** | AI-assisted coding |
| **Figma** | UI/visual design |
| **Python** | Scripting & data tooling |

## Hosting & Infrastructure

| Tool | Role |
|---|---|
| **Hostinger VPS** | Self-hosted n8n production instance *(evidence-based)* |
| **Cloudflare** | DNS / edge (where applicable) |

---

### Stack Philosophy

We deliberately self-host the automation core (n8n on VPS) for **cost control, data ownership, and reliability**, while leaning on managed APIs (OpenAI, Anthropic, Retell, Twilio, Cal.com) for the components where managed services win. Model selection is matched to each task — small models for classification/drafting, frontier models for reasoning — to keep running costs low without sacrificing quality.
