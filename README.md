# KOINO Skills — Free Agent Skills for Business Automation

> 10 production-tested skills for sales, content, operations, and growth.
> Compatible with Claude Code, Codex, Gemini CLI, Cursor, and 30+ AI agents.

## Skills

| Skill | Category | What It Does |
|-------|----------|-------------|
| [sales-objection-coach](./sales-objection-coach) | Sales | Responds to objections with psychology-backed L.M.C. framework |
| [content-qa-scorer](./content-qa-scorer) | Content | Scores content on 7 dimensions: PASS / NEEDS WORK / KILL |
| [lead-scorer](./lead-scorer) | Sales | Scores prospects 0-100 with configurable rubric |
| [daily-brief-generator](./daily-brief-generator) | Operations | Generates structured daily business briefings |
| [cold-email-writer](./cold-email-writer) | Sales | Writes personalized cold emails (3-5 sentences, one CTA) |
| [proposal-generator](./proposal-generator) | Sales | Generates service proposals from client details |
| [rep-performance-tracker](./rep-performance-tracker) | Management | Tracks rep metrics, scores churn risk |
| [agent-fleet-status](./agent-fleet-status) | DevOps | Health dashboard for distributed agent systems |
| [cron-automator](./cron-automator) | DevOps | Generates cron configurations for automation patterns |
| [competitor-analyzer](./competitor-analyzer) | Research | Analyzes competitor positioning, pricing, weaknesses |

## Install

```bash
# Install a single skill
npx skills add koinod/koino-skills/<skill-name>

# Or clone the repo
git clone https://github.com/koinod/koino-skills.git
cp -r koino-skills/<skill-name> ~/.claude/commands/
```

## Usage

Each skill activates automatically based on context. For example:

- **Ask about handling a sales objection** → `sales-objection-coach` activates
- **Paste content for review** → `content-qa-scorer` activates
- **Describe a new lead** → `lead-scorer` activates

Skills work best when installed together — they complement each other.

## Want These Running Autonomously?

These skills are designed to be useful one-off. But what if they ran **24/7 without you**?

**[KOINO Deploy](https://koino.capital/deploy)** takes these capabilities and deploys them as autonomous agent fleets on your infrastructure. Scoring every lead. Coaching every rep. Processing every piece of content. All day, every day.

[See what a deployment looks like →](https://koino.capital/case-study)

## About

Built by [KOINO Capital](https://koino.capital) — we build autonomous AI growth systems for businesses.

These skills are extracted from systems we run in production. Not theory. Not templates. Real operations.

## License

MIT — use them however you want. If they help your business, consider [deploying the full system](https://koino.capital/deploy).
