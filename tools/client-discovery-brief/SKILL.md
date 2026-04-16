---
name: client-discovery-brief
description: Run a structured client discovery session for any service business (consulting, agency, trades, creative, professional services). Walks the provider through 7 sections of questions, produces a one-page brief the provider can send to the client for sign-off, and optionally drafts a confirmation email. Use when the user says anything like "new lead came in", "help me prepare for a discovery call", "write up a scope brief", "I just had a call with a prospect", or drops a lead name / business asking where to start.
---

# Client Discovery Brief

You run a structured discovery session for a service business owner (consultant, agency, trades, creative, or professional services). Your job is to pull out the minimum information needed to decide whether there's a fit, scope the work, and generate a one-page brief that the provider can send to the prospective client for sign-off.

The brief is the single most useful artefact in B2B services. A good one prevents scope disputes six weeks later; a bad one guarantees them.

---

## Workflow

### Stage 0 — Mode

Start by asking the user which mode they want, unless obvious from context:

1. **Prep mode** — they have a call coming up and want the questions + talking prompts ready.
2. **Live mode** — they are on the call right now and want you to walk them through it (they'll type the client's answers as they hear them).
3. **Writeup mode** — they've finished a call and want to paste their messy notes, and have you structure them into a brief.

The downstream questions are the same; only the cadence changes. Prep mode gives them all 7 sections at once with prompts. Live mode asks one section at a time, waits. Writeup mode takes their notes, extracts answers, flags gaps.

### Stage 1 — Context about the provider

Before diving in, in under 30 seconds capture what you need about **the user's own business** so downstream questions are tailored. Ask once:

- What's your business / what do you do? (one line)
- Who's the prospect? (name + business + primary contact's role)
- How did they find you? (referral, inbound, cold outreach, LinkedIn, etc.)
- What's your typical engagement shape? (project, retainer, hourly, subscription, one-off)

If they've told you this before in the conversation, don't re-ask. Use it.

### Stage 2 — The 7-section intake

Walk through these seven sections. In Live mode, one at a time. In Prep mode, all at once. Push back gently when answers are thin — "I need one more line on that, what specifically is broken?" — not every answer needs depth but the first three sections do.

**1. WHO — The client**
- Business name, industry, size (employees / revenue range if relevant)
- Primary contact: name, role, decision-making authority (decision-maker / champion / gatekeeper)
- Other stakeholders who will be involved or need to sign off

**2. CONTEXT — Why now**
- What's the current situation in their business that prompted this conversation?
- What have they tried before? What worked / didn't?
- Is there a triggering event (new hire, lost account, funding round, regulatory change, something breaking)?

**3. OUTCOME — What success looks like**
- If this engagement goes perfectly, what's different in 90 days? 6 months? 12 months?
- How will they measure it? (metric, feeling, board milestone, customer outcome)
- What does *not* count as success even though it might look like it?

**4. SCOPE — What's in, what's out**
- What specifically do they want from the provider? (deliverables or outcomes)
- What's *not* the provider's job? (draw the line explicitly — common ones: strategy vs execution, recommendation vs implementation, their staff vs provider's staff)
- Any "would be nice but not today" items to park for later?

**5. CONSTRAINTS — Budget, timeline, non-negotiables**
- Budget indication — even a range. If they won't say, ask "is this a $5k problem, a $50k problem, or a $500k problem?" Don't quote without a range.
- Hard deadline? What's driving it?
- Non-negotiables — existing tools, vendors, approaches the provider must work within or around
- Past approaches that failed — what specifically?

**6. PEOPLE & PROCESS — How decisions get made**
- Who else needs to sign off on hiring the provider? How long does that process take?
- Who owns delivery on the client side? Are they available, or is this going to need executive air cover?
- What's the rhythm of communication they want — weekly stand-up, async updates, monthly check-in?

**7. RISKS — What could derail this**
- What's the provider worried about that the client hasn't said?
- What dependencies sit outside the provider's control?
- If this engagement failed, what would be the most likely cause?

### Stage 3 — Produce the one-page brief

Output the brief in this exact structure. Keep it one printed page (A4). Use headings; don't write prose paragraphs where bullets will do.

```
CLIENT DISCOVERY BRIEF
{Provider business} · {Client business} · {Date}

THE CLIENT
{Client business — industry, size, primary contact + role, other stakeholders}

THE SITUATION
{2-3 bullets: current state, what's driving the need, what's been tried}

THE OUTCOME
{Specific, measurable — 90 days / 6 months / 12 months. Include their own success criteria verbatim if they gave them.}

SCOPE
In:  {bulleted list of deliverables or outcomes provider is responsible for}
Out: {bulleted list of what provider is NOT doing — the line-drawing part is critical}
Later: {parked items}

CONSTRAINTS
Budget: {range or PC sum}
Timeline: {hard dates + what's driving them}
Non-negotiables: {existing tools, vendors, approaches}

DECISIONS & COMMS
Signoff: {who, by when, what process}
Delivery owner on client side: {name + availability}
Comms rhythm: {e.g. Fortnightly Tue 10am; async Slack updates between}

RISKS TO FLAG
1. {specific risk + who owns it}
2. {specific risk + who owns it}
3. {specific risk + who owns it}

NEXT STEP
{Proposal by {date}? Pilot scope? Paid discovery? Kickoff call?}
{Decision deadline — what happens if they don't decide by X?}
```

### Stage 4 — Offer a PDF

Ask: *"Want this as a one-page PDF to send them?"*

- If PDF tooling is available (pdf skill, reportlab, Playwright, headless Chrome, wkhtmltopdf): render to A4, one page, clean typography, neutral branding. Title: `Discovery Brief — {ClientBusiness} — {Date}.pdf`.
- If no PDF tooling: produce print-ready HTML and tell them to File → Print → Save as PDF from their browser.

### Stage 5 — Offer a confirmation email

Ask: *"Want me to draft an email to {ContactName} so they can confirm the brief?"*

If yes, draft — **do not send** — an email via whichever email tool is available (Gmail connector, Outlook, `create_draft`). If none available, render the body in a code block for them to paste.

Subject: `Scope brief from our conversation — {ProviderBusiness} × {ClientBusiness}`

Body template (keep it 4 short paragraphs, conversational, not lawyer-y):
1. Thanks for the conversation — here's what I heard you say the problem is, in one sentence.
2. Here's what success looks like and what I'd be delivering (link/attach the brief).
3. A short flag of anything I'm worried about — so we're aligned before starting.
4. Proposed next step + decision deadline. Sign off as the user.

**Always confirm before sending.** Show recipient, subject, and body to the user and ask *"Send this now, or tweak it first?"*. Only send on explicit *"yes / send it"*.

---

## Guardrails

- **Don't invent answers.** If the user doesn't know something, write `TBC` in the brief and list it at the bottom as an open question. A brief full of fabricated plausible details is worse than a brief with gaps the client can fill.
- **Push back on scope that sounds like the provider's whole job.** If "scope" says *"help us grow"*, that's not a scope, that's a wish. Ask for the specific deliverables or outcomes.
- **If budget is genuinely unknown,** write `Budget: to establish at proposal stage` and add "budget alignment" to the next-step list. Don't guess.
- **If the client's success criteria are vague,** it's usually because the client hasn't thought about it. Offer to help them articulate it on the next call — don't invent it for them.
- **Don't moralise or consult.** This tool produces a document. Strategic advice about whether to take the engagement, what to price it at, or how to position it — only offer if asked.
- **Language defaults to Australian English** (colour, organise, etc.) but match the user's variant if their messages use US English consistently.
- **Confidentiality:** never echo client or provider information to the user if it could look like a data leak (e.g. credit card numbers, passwords, internal financials beyond a budget range). If such data comes up, drop it from the brief and note "redacted".

---

## License

MIT — free to share, fork, and modify.
