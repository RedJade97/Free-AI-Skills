# Subbie Scoping Brief — AU

A zero-install scoping-call assistant for builders, developers, and site PMs engaging subcontractors.

**What it does:** paste one markdown file into your own Claude account. Before you lock in a subbie, Claude walks you through a 7-section structured conversation — scope, programme, materials, commercials, insurance, references, risks — and produces a one-page engagement brief you can drop straight into your project file or use as the basis for a subcontract.

Works three ways:
- **Prep mode** — call coming up; Claude gives you the full question list + talking prompts
- **Live mode** — on the call right now; Claude asks one section at a time while you type in what the subbie says
- **Writeup mode** — call's done, paste your messy notes, Claude structures them and flags gaps

**Why it exists:** a good scoping call prevents the three most expensive surprises on any build — variations argued about as "extras", programme blowouts from over-booked subbies, and defects disputes at PC because scope wasn't written down. This skill is designed to surface all three before you pay a deposit.

**What it costs you:** nothing. No login, no server, no API key.

---

## How to use it

### Option A — Claude.ai Projects (easiest)

1. Open [SKILL.md](SKILL.md), copy the contents.
2. [claude.ai](https://claude.ai) → new Project called "Subbies".
3. Paste into **Custom Instructions**.
4. New subbie on the horizon → open a chat in that project and say *"I'm chasing a quote from a concreter for the Bellevue Hill job"* or similar. It'll take it from there.

### Option B — Claude Desktop / Claude Code skills

1. Download this `subbie-scoping-brief` folder.
2. Drop into your Claude skills directory.
3. Trigger with *"calling a subbie"* / *"pricing conversation with a [trade]"*.

### Option C — One-shot paste

Copy everything below the `---` frontmatter in [SKILL.md](SKILL.md) into any Claude chat, then say who the subbie is.

---

## The 7 sections

1. **Scope** — inclusions, exclusions, supply split, drawings reference
2. **Lead time & programme** — start date, duration, concurrent jobs, crew size
3. **Materials** — specific brands/SKUs, lead times, substitutions, warranties
4. **Commercials** — ex-GST quote, ABN, payment terms, retention, variation rates, rise-and-fall
5. **Insurance, licensing, compliance** — public liability, workers comp, trade licence, SWMS, White Card
6. **References & track record** — two recent similar jobs, dispute history, walk-one-job option
7. **Risks** — programme, quality, anything in the subbie's tone that felt off

## What you get back

- **One-page engagement brief** in standard structure — drops straight into your project file or forms the basis for a subcontract
- **Optional PDF** for the project folder
- **Optional RFQ document** if you're still quote-shopping and want to send a consistent brief to 2–3 more subbies
- **Follow-up email draft** — engagement-intent / clarification / pass (never burn a subbie bridge on a no)

## Hard gates built in

- **No subcontract until COIs + licence are sighted** — the skill flags missing insurance/licence data and defaults the recommendation to "second-quote" or "pass" until they're provided.
- **T&M without a cap triggers a loud warning** — uncapped time-and-materials on a fixed-price head contract is how builders go broke.
- **Compliance defaults to AU** — HIA/MBA contracts, NCC 2022, WHS regs, Security of Payment Act, state-specific licensing.

## Caveats

The engagement brief is **indicative** — it's your scoping record, not a contract. Always flow into a proper AS4903 (or HIA / MBA equivalent) subcontract before handing over a deposit. If a dispute does arise, Security of Payment Act timelines are unforgiving — check with a solicitor, not Claude.

## License

MIT.
