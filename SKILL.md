# KOINO Skills Suite

> A collection of 10 production-grade business skills covering sales, content, operations, and competitive research. Install this meta-skill to get all 10.

## Description

KOINO Skills Suite is a comprehensive set of AI agent skills built for businesses doing $250K-$5M in annual revenue. Each skill handles a specific business function — from qualifying leads to writing cold emails to monitoring server fleets. They work independently or as an integrated system.

This is the meta-skill. Installing it gives your agent access to all 10 specialized skills.

## Activation

This skill activates when:
- The user asks for help with any business operations task
- The user mentions sales, content, leads, proposals, outreach, scheduling, or competitive analysis
- The user wants to automate or systematize a business process
- The user asks "what can you help me with?"

The meta-skill routes to the appropriate specialized skill based on context.

## Included Skills

### Sales & Revenue
| Skill | Trigger | What You Get |
|-------|---------|-------------|
| **sales-objection-coach** | Prospect says "no" or pushes back | L.M.C. framework response + psychology breakdown |
| **lead-scorer** | New prospect to evaluate | 0-100 score: HOT / WARM / COLD / DISQUALIFIED |
| **cold-email-writer** | Need to reach out to a prospect | 3-5 sentence P.A.S. email ready to send |
| **proposal-generator** | Ready to send a formal offer | Complete proposal with 3 pricing tiers |
| **rep-performance-tracker** | Check sales metrics or team performance | Scorecard with grades, trends, and churn risk |

### Content & Marketing
| Skill | Trigger | What You Get |
|-------|---------|-------------|
| **content-qa-scorer** | Draft content needs review | 7-dimension score: PASS / NEEDS WORK / KILL |
| **competitor-analyzer** | Need competitive intelligence | Full report: positioning, pricing, weaknesses, gaps |

### Operations & Infrastructure
| Skill | Trigger | What You Get |
|-------|---------|-------------|
| **daily-brief-generator** | Start of day or need status overview | 2-minute briefing: revenue, fires, priorities, pipeline |
| **agent-fleet-status** | Check on servers or distributed systems | Health dashboard: disk, memory, CPU, services, alerts |
| **cron-automator** | Schedule a recurring task | Correct cron expression with logging and error handling |

## Routing Logic

When a request comes in, the meta-skill routes based on keywords:

```
"objection" / "they said no" / "handle this"     → sales-objection-coach
"score this" / "review" / "QA" / "is this good"  → content-qa-scorer
"qualify" / "is this worth" / "score this lead"   → lead-scorer
"morning brief" / "daily" / "what should I do"    → daily-brief-generator
"cold email" / "outreach" / "reach out to"        → cold-email-writer
"proposal" / "quote" / "SOW"                      → proposal-generator
"close rate" / "sales metrics" / "performance"    → rep-performance-tracker
"fleet" / "server status" / "check my machines"   → agent-fleet-status
"cron" / "schedule" / "run every"                 → cron-automator
"competitor" / "compare" / "positioning"           → competitor-analyzer
```

If the request spans multiple skills, chain them:
- "Score this lead and write a cold email" → lead-scorer then cold-email-writer
- "Check fleet status and generate my morning brief" → agent-fleet-status then daily-brief-generator
- "Analyze the competitor and write a proposal that beats them" → competitor-analyzer then proposal-generator

## Example Workflow

### Full Sales Cycle in 5 Minutes

1. **Lead comes in** → `lead-scorer` qualifies them (Score: 74, WARM)
2. **Write outreach** → `cold-email-writer` generates personalized email
3. **They reply with objection** → `sales-objection-coach` provides L.M.C. response
4. **Meeting goes well** → `proposal-generator` creates 3-tier proposal
5. **They mention a competitor** → `competitor-analyzer` provides counter-positioning
6. **Deal closes** → `rep-performance-tracker` updates metrics

Total time: 5 minutes of AI-assisted work instead of 3 hours of manual effort.

### Daily Operations Loop

1. **8:00 AM** → `daily-brief-generator` produces morning briefing
2. **8:05 AM** → `agent-fleet-status` confirms all systems running
3. **9:00 AM** → `content-qa-scorer` reviews today's scheduled content
4. **10:00 AM** → `lead-scorer` prioritizes new inbound leads
5. **2:00 PM** → `cold-email-writer` generates afternoon outreach batch
6. **5:00 PM** → `rep-performance-tracker` generates end-of-day scorecard

## Installation

### All Skills at Once
```bash
# Claude Code
claude install-skill github.com/koino-capital/koino-skills-public

# Manual
git clone https://github.com/koino-capital/koino-skills-public.git
```

### Individual Skills
Each skill is in its own directory with a self-contained SKILL.md. Install only what you need.

## Requirements

- Any AI agent that reads SKILL.md files (Claude Code, Codex, Gemini CLI, Cursor, Windsurf, etc.)
- No API keys
- No dependencies
- No setup

---

*Built by [KOINO Capital](https://koino.capital) — Agentic growth systems that run while you sleep.*
*Want this running autonomously 24/7? [Deploy with KOINO](https://koino.capital/deploy)*
