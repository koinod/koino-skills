# KOINO Skills — Free Agent Skills for Business Automation

> 14 production-tested skills for sales, content, operations, and growth.
> Compatible with Claude Code, Codex, Gemini CLI, Cursor, Windsurf, and 30+ AI agents.

> **Looking for the full operational fleet?** This repo is the public-facing trim subset (14 polished skills for distribution). The complete 76-skill master operational repo is at **[koinod/skills](https://github.com/koinod/skills)** — that's where koinod fleet agents go to find capabilities and save new ones. Failure log + patterns at **[ceoian/agent-learnings](https://github.com/ceoian/agent-learnings)**.

## Skills

| # | Skill | Category | What It Does |
|---|-------|----------|-------------|
| 1 | [sales-objection-coach](./sales-objection-coach) | Sales | Handle any objection with the L.M.C. framework + psychology |
| 2 | [content-qa-scorer](./content-qa-scorer) | Content | Score content on 7 dimensions: PASS / NEEDS WORK / KILL |
| 3 | [lead-scorer](./lead-scorer) | Sales | Score prospects 0-100 — HOT / WARM / COLD / DISQUALIFIED |
| 4 | [daily-brief-generator](./daily-brief-generator) | Operations | Morning business briefing from any data sources |
| 5 | [cold-email-writer](./cold-email-writer) | Sales | Personalized cold emails using P.A.S. + 1 CTA formula |
| 6 | [proposal-generator](./proposal-generator) | Sales | Service proposals in 60 seconds from client details |
| 7 | [rep-performance-tracker](./rep-performance-tracker) | Management | Sales metrics, close rates, pipeline velocity, churn risk |
| 8 | [agent-fleet-status](./agent-fleet-status) | DevOps | Multi-machine health dashboard via SSH |
| 9 | [cron-automator](./cron-automator) | DevOps | Generate cron jobs from plain English scheduling requests |
| 10 | [competitor-analyzer](./competitor-analyzer) | Research | Competitive intelligence: pricing, features, weaknesses |
| 11 | [ai-cold-email](./ai-cold-email) | Sales | Generate personalized cold outreach emails |
| 12 | [content-repurpose](./content-repurpose) | Content | Turn transcripts into social media posts |
| 13 | [workflow-auditor](./workflow-auditor) | Operations | Audit workflows and find automation opportunities |
| 14 | [roi-calculator](./roi-calculator) | Finance | Calculate AI automation ROI |

## Install

### Claude Code
```bash
# Install all skills at once
claude install-skill github.com/koino-capital/koino-skills-public

# Install a single skill
claude install-skill github.com/koino-capital/koino-skills-public/sales-objection-coach
```

### Codex / Gemini CLI / Cursor
Copy the `SKILL.md` from any skill directory into your project's `.skills/` or `.cursor/skills/` directory. The agent auto-detects it.

### Manual / Any Agent
Clone the repo and point your agent at the SKILL.md files:
```bash
git clone https://github.com/koino-capital/koino-skills-public.git
cp -r koino-skills-public/<skill-name>/SKILL.md ~/.claude/commands/
```

Each SKILL.md is self-contained — no dependencies, no API keys, no setup.

## Usage

Skills activate automatically based on context:

- **Mention a sales objection** → `sales-objection-coach` fires
- **Paste content for review** → `content-qa-scorer` scores it
- **Describe a new lead** → `lead-scorer` qualifies them
- **Ask for a morning briefing** → `daily-brief-generator` builds it
- **Need to reach out cold** → `cold-email-writer` drafts the email
- **Closing a deal** → `proposal-generator` creates the proposal

Skills work individually or as a suite. Together, they cover the full business cycle: prospect, qualify, outreach, propose, close, deliver, optimize.

## Why These Skills?

These are not toy demos. Each skill is extracted from real systems running in production:

- **sales-objection-coach** — built from 1,000+ analyzed sales calls
- **content-qa-scorer** — gates content before it goes live for paying clients
- **lead-scorer** — prioritizes a live pipeline of 21+ prospects daily
- **daily-brief-generator** — runs every morning across a 4-machine agent fleet
- **agent-fleet-status** — monitors distributed agents running 24/7

Every skill is opinionated. They tell you what to do, what NOT to do, and why.

## Philosophy

1. **Useful first.** If a skill doesn't save time or make money, it shouldn't exist.
2. **Opinionated.** Generic advice is useless. These skills take a position.
3. **Complete.** Instructions, examples, inputs, outputs. No "coming soon."
4. **Zero dependencies.** No API keys, no packages, no setup.
5. **Cross-platform.** Any agent that reads markdown can use these.

## Want These Running Autonomously?

These skills are designed to be useful as one-off tools. But what if they ran **24/7 without you**?

**[KOINO Deploy](https://koino.capital/deploy)** takes these skills and deploys them as autonomous agent fleets on your infrastructure. Scoring every lead. Coaching every rep. Processing every piece of content. All day, every day.

[See what a deployment looks like](https://koino.capital/case-study)

## Contributing

PRs welcome. Keep the format consistent:
- Clear activation triggers
- Structured output templates
- Real examples (not hypothetical)
- Actionable instructions, not theory

## License

MIT — use them however you want. If they help your business, consider [deploying the full system](https://koino.capital/deploy).

---

Built by [KOINO Capital](https://koino.capital) — Agentic growth systems that run while you sleep.
