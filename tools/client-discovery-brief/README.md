# Client Discovery Brief

A zero-install discovery-call assistant for any service business — consultants, agencies, trades, creatives, professional services.

**What it does:** you paste one markdown file into your own Claude account. When a new prospect lands, Claude walks you through a 7-section intake (who, context, outcome, scope, constraints, people/process, risks), produces a one-page scope brief you can send to the client for sign-off, and drafts a confirmation email.

Works three ways:
- **Prep mode** — you're about to take a call; Claude gives you the full question list and talking prompts
- **Live mode** — you're on the call right now; Claude asks one section at a time while you type in answers
- **Writeup mode** — you finished the call, paste your messy notes, Claude structures them and flags gaps

**What it costs you:** nothing. No login, no server, no API key.

---

## How to use it

### Option A — Claude.ai Projects (easiest)

1. Open [SKILL.md](SKILL.md) and copy the entire contents.
2. Go to [claude.ai](https://claude.ai), create a new Project called "Discovery".
3. Paste the contents into **Custom Instructions**.
4. Any new lead comes in, open a new chat in that project and say *"new lead — [name]"* or *"prep me for a discovery call with [name]"*.

### Option B — Claude Desktop / Claude Code skills

1. Download this `client-discovery-brief` folder.
2. Drop into your Claude skills directory.
3. Trigger with *"new lead just came in"* or *"write up this discovery call"*.

### Option C — One-shot in any Claude chat

Copy everything below the `---` frontmatter line in [SKILL.md](SKILL.md), paste into a chat, then say what you want (prep, live, or writeup).

---

## The 7 sections you'll be asked about

1. **Who** — the client, contact, stakeholders
2. **Context** — why now, what's been tried
3. **Outcome** — what success looks like at 90 days / 6 months / 12 months
4. **Scope** — what's in, what's out, what's parked
5. **Constraints** — budget range, timeline, non-negotiables
6. **People & process** — signoff path, delivery owner, comms rhythm
7. **Risks** — what could derail this

## What you get back

- A one-page brief in a standard structure (Client / Situation / Outcome / Scope / Constraints / Decisions & Comms / Risks / Next Step)
- Optional PDF export
- Drafted confirmation email to the client

## Why a brief matters

In B2B services, the brief is the single most useful artefact in the engagement. A good one prevents scope disputes six weeks later. A bad one guarantees them. Taking 20 minutes to put one together pays back every hour you don't spend arguing about "I thought that was included."

## License

MIT.
