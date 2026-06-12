# Monthly Technology Investment

An estimate of Daigon's recurring software/tooling spend to operate the automation practice. This demonstrates a lean, high-leverage stack — most costs are **usage-based** and scale with client volume (i.e. they grow only as revenue grows).

> ⚠️ **All figures are estimates.** Exact amounts vary with plan tier and usage. USD primary; ZAR ≈ R18.3/USD. "Variable" = usage-based and client-funded in most engagements.

---

## Core Recurring Stack

| Tool | Purpose | Monthly (USD, est.) | Monthly (ZAR, est.) | Annual (USD, est.) | Business Value | Critical / Optional |
|---|---|---|---|---|---|---|
| **VPS hosting (Hostinger)** | Self-hosted n8n production server | $15–$40 | R275–R730 | $180–$480 | Owns the automation engine; no per-task SaaS fees | **Critical** |
| **n8n** | Workflow automation (self-hosted = free core) | $0–$50 | R0–R915 | $0–$600 | Orchestration backbone | **Critical** |
| **OpenAI API** | GPT-4o/4.1/5 reasoning & generation | $20–$150* | R366–R2,745 | $240–$1,800 | Core agent intelligence | **Critical** |
| **Anthropic Claude API** | Claude Sonnet 4 reasoning/drafting | $15–$100* | R275–R1,830 | $180–$1,200 | Secondary/long-context model | Critical |
| **Retell AI** | AI voice agents (per-minute) | $30–$200* | R549–R3,660 | $360–$2,400 | Voice agent runtime | Critical (voice clients) |
| **Vapi** | Alternative voice runtime | $0–$80* | R0–R1,464 | $0–$960 | Voice flexibility | Optional |
| **Twilio** | SMS & voice transport | $20–$150* | R366–R2,745 | $240–$1,800 | Missed-call/SMS delivery | Critical (SMS clients) |
| **ElevenLabs** | AI voice (TTS) | $5–$99 | R92–R1,812 | $60–$1,188 | Natural voice output | Optional |
| **WhatsApp Business API** | Conversational messaging | $0–$80* | R0–R1,464 | $0–$960 | WhatsApp agents (per-conversation) | Critical (WA clients) |
| **Cal.com** | Booking/scheduling | $0–$15 | R0–R275 | $0–$180 | Appointment lifecycle | Critical (booking clients) |
| **Google Workspace** | Email, Sheets, Docs, Calendar | $7–$18 | R128–R329 | $84–$216 | Data source-of-truth & comms | **Critical** |
| **Airtable** | Structured CRM/pipeline data | $0–$24 | R0–R439 | $0–$288 | Client data management | Optional |
| **Notion** | Knowledge base & ops | $0–$12 | R0–R220 | $0–$144 | Internal/agency knowledge | Optional |

\* *Usage-based — typically funded by or rebilled to the client in active engagements.*

## Developer / Design Tooling

| Tool | Purpose | Monthly (USD, est.) | Monthly (ZAR, est.) | Critical / Optional |
|---|---|---|---|---|
| **Claude Code / Claude (Pro/Max)** | AI build automation & engineering | $20–$200 | R366–R3,660 | Critical |
| **Cursor** | AI-assisted coding | $0–$20 | R0–R366 | Optional |
| **GitHub** | Version control | $0–$4 | R0–R73 | Optional |
| **Figma** | UI/visual design | $0–$15 | R0–R275 | Optional |
| **Cloudflare** | DNS/edge | $0–$20 | R0–R366 | Optional |

---

## Estimated Totals

| Scenario | Monthly (USD, est.) | Monthly (ZAR, est.) | Annual (USD, est.) |
|---|---|---|---|
| **Lean / baseline** (fixed tooling, low usage) | **≈ $90–$150** | **≈ R1,650–R2,750** | **≈ $1,080–$1,800** |
| **Active** (several live clients, moderate usage) | **≈ $250–$500** | **≈ R4,600–R9,150** | **≈ $3,000–$6,000** |
| **Scaled** (many voice/SMS clients, high volume) | **≈ $600–$1,200+** | **≈ R11,000–R22,000+** | **≈ $7,200–$14,400+** |

---

## Key Takeaways

- **The fixed cost base is tiny.** Self-hosting n8n on a VPS replaces what would otherwise be hundreds of dollars in per-task SaaS automation fees.
- **Most spend is variable and client-funded.** AI tokens, voice minutes, and SMS scale with client volume — so cost rises only alongside revenue.
- **High margin by design.** A single retained client typically covers the entire fixed monthly stack several times over.
