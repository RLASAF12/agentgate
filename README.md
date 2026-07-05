# AgentGate ⛩

**Human-in-the-loop approval cards for AI agent actions.**

> *Before the agent acts, you decide.*

[![Live Demo](https://img.shields.io/badge/Live%20Demo-agentgate-indigo?style=flat-square)](https://rlasaf12.github.io/agentgate/)

---

## What is it?

AI agents are taking real actions — sending emails, deleting files, making transfers, posting publicly — and most teams have no approval layer in front of them.

AgentGate is a single-page tool that surfaces a structured **approval card** before any consequential agent action executes. You see exactly:

- What the agent is about to do (plain English)
- Why the agent decided to do it (its reasoning)
- Concrete outcomes if you approve or reject
- Risk classification (Low / Medium / High) with a one-line justification
- The system's recommendation (Approve / Reject / Review first)

One tap. Approve or reject. Decision logged.

---

## Why it exists

**96%** of developers say they don't fully trust AI agent output. **47%** of CISOs reported unauthorized agent behavior in the past year *(Saviynt, 2026)*. The META incident (Feb 2026) showed agents will ignore "suggest only" instructions and take irreversible action anyway.

The frameworks trust the agent. AgentGate doesn't — and makes that explicit.

---

## What's inside

```
agentgate/
└── index.html          # The entire app — no build step, no dependencies
```

Single-file. Pure HTML + Tailwind CDN + Gemini REST API. No backend. No data stored anywhere.

---

## Quick start

**Option 1 — just open it:**
```
https://rlasaf12.github.io/agentgate/
```

**Option 2 — run locally:**
```bash
# Clone
git clone https://github.com/RLASAF12/agentgate.git
cd agentgate

# Open in browser (no server required)
open index.html
```

---

## How to use

**Without an API key (5 built-in demos):**
Click any scenario chip — *Client email, Delete files, Deactivate account, LinkedIn post, Wire transfer* — and get a pre-built approval card instantly.

**With a Gemini API key (custom scenarios):**
1. Click **⚙ API Key** in the header
2. Paste your free [Gemini API key](https://aistudio.google.com/app/apikey)
3. Type any agent action in the text box and click **Generate Approval Card**

The key is stored only in your browser's `localStorage`. Nothing is sent to any server except Gemini.

---

## The approval card

Each card includes:

| Section | What it shows |
|---------|---------------|
| **Action summary** | What the agent is about to do, in one sentence |
| **Risk badge** | 🟢 Low / 🟡 Medium / 🔴 High, with a one-line reason |
| **Risk bar** | Visual indicator of risk severity |
| **Agent reasoning** | Why the agent decided to take this action |
| **If approved** | Concrete outcomes if you say yes |
| **If rejected** | What happens instead — the real fallback |
| **Recommendation** | Approve / Reject / Review, with reasoning |
| **Context note** | Optional free-text note before you decide |
| **Decision log** | Full session history with timestamps |

---

## Built with

- [Tailwind CSS CDN](https://tailwindcss.com) — styling
- [Gemini 2.0 Flash](https://ai.google.dev) — card generation for custom scenarios
- Zero dependencies. Zero backend. Zero build step.

---

## Related

Built as part of Harel Asaf's AI agent infrastructure series.

- [harelasaf.com](https://harelasaf.com)
- [AgentCharter](https://rlasaf12.github.io/agent-charter/) — AI governance charter generator
- [FlowDraft](https://rlasaf12.github.io/flowdraft/) — process description → workflow spec

---

*Security checklist passed — 2026-07-06. No credentials, no personal data, no internal paths in published code.*
