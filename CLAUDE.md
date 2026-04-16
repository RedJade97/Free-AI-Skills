# Free AI Skills — repo notes for Claude

## Project intent
This repo is a collection of free Claude Skills for small business owners, distributed primarily through LinkedIn. Each skill is a single `SKILL.md` file that users paste into their own Claude account. No login, no server, no API key — their data stays in their own Claude chat.

## How to work in this repo

- **Default output format for a new tool is a Claude Skill** (`tools/<tool-name>/SKILL.md` with frontmatter). Only fall back to a React/Python/Excel build when a skill genuinely can't do the job (e.g. bulk data crunching, real-time integrations, offline use).
- **Audience is non-technical.** Every tool README must start with a "how to use it in 30 seconds" section. No `npm install` in the critical path.
- **Keep disclaimers on anything that touches money.** Estimators, calculators, and P&L templates all need an "indicative only" note.
- **Australian defaults** unless told otherwise — rates, currency (AUD), compliance language (HIA, NatHERS, BAL, NCC, etc.).

## Workflow preferences

- Keep executing. Don't pause for routine confirmation. Only pause before: large architectural decisions, destructive ops (rm -rf, force-push), sending/publishing, or installing large toolchains. Small reversible choices — just pick and note it in the summary.
- Prefer additive changes over rewrites. The goal is a steadily growing library, not a perfectly designed monorepo.
- Don't add tooling, CI, or package scaffolding until there's a reason to.

## Structure

```
Free-AI-Skills/
├── tools/        # Claude skills (primary output)
├── templates/    # Excel / Google Sheets templates
├── scripts/      # Standalone Python / shell scripts
├── web/          # Browser-hosted tools (HTML/JS, GitHub Pages)
└── README.md     # Landing page — keep the skill list current
```

When you add a new skill, update the `README.md` table and the "Coming soon" list.
