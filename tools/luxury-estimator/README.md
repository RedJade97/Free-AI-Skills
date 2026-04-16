# Luxury Home Estimator — Australia

A zero-install estimator for high-end residential builds in Sydney, Melbourne, Brisbane, Perth, Adelaide, Gold Coast, and Canberra.

**What it does:** you paste one markdown file into your own Claude account. Claude walks you through a short questionnaire, produces a costed estimate (range, trade breakdown, risks, value-engineering moves, timeline, market notes), offers to compile it as a PDF, and can draft an email to your project manager for you to send.

**What it costs you:** nothing. No login, no server, no API key. Uses whichever Claude account you already have.

---

## How to use it

Pick whichever applies.

### Option A — Claude.ai Projects (easiest, no technical setup)

1. Open [SKILL.md](SKILL.md) and copy the entire contents.
2. Go to [claude.ai](https://claude.ai), create a new Project.
3. Paste the contents into **Custom Instructions**.
4. In any new chat inside that project, type *"I need an estimate for a luxury build"* and it will take it from there.

### Option B — Claude Desktop / Claude Code skills

1. Download the `luxury-estimator` folder.
2. Drop it into your Claude skills directory (`~/.claude/skills/` on macOS/Linux, `%USERPROFILE%\.claude\skills\` on Windows).
3. Restart Claude. Ask: *"estimate a luxury build"* and the skill will trigger.

### Option C — One-shot in any Claude chat

1. Open [SKILL.md](SKILL.md).
2. Copy everything below the `---` frontmatter line.
3. Paste it into any Claude chat as your first message, followed by your project brief. Claude will run the estimator immediately.

---

## What you'll be asked

12 quick questions — city, floor area, storeys, quality tier, site condition, beds, baths, pool, smart-home, sustainability, garage bays, basement. Takes ~2 minutes.

## What you get back

- Headline cost range (low / mid / high) in AUD
- Cost per m²
- Breakdown by construction / addons / fees / permits / contingency
- 9-trade breakdown (structure, envelope, roofing, fitout, kitchen, bathrooms, electrical, plumbing, landscaping)
- Top 3 cost risks with mitigations
- Top 3 value-engineering moves with dollar savings
- Timeline in weeks
- City-specific market commentary
- PDF export
- Drafted email for your PM

## Caveats

These figures are **indicative only.** They are built from published 2025/26 rate data (HIA, Rawlinsons, ABS, Altus) and are useful for early-stage feasibility and client conversations. Always engage a licensed builder and quantity surveyor before you commit to a budget.

## License

MIT.
