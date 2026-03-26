# Rep Performance Tracker

> Track sales rep metrics: calls, close rate, pipeline value, and churn risk scoring.

## Description

Rep Performance Tracker turns raw sales activity data into actionable performance dashboards. It calculates close rates, pipeline velocity, activity ratios, and flags reps at risk of churning or underperforming — before it shows up in revenue. Works for solo operators tracking their own metrics or managers overseeing a team.

## Activation

This skill activates when:
- The user wants to track or analyze sales performance metrics
- The user provides sales activity data (calls, closes, pipeline)
- The user asks about close rates, conversion rates, or sales efficiency
- The user mentions rep performance, sales leaderboard, or activity tracking

**Trigger phrases**: "track my sales", "close rate", "rep performance", "sales metrics", "pipeline velocity", "how am I doing", "sales dashboard", "conversion rate", "activity report"

## Core Metrics

### Activity Metrics (Leading Indicators)
| Metric | Formula | Benchmark |
|--------|---------|-----------|
| **Calls/Day** | Total calls / days worked | 25-50 (outbound), 10-20 (closing) |
| **Emails Sent/Day** | Total emails / days worked | 30-60 (SDR), 10-20 (AE) |
| **Meetings Booked/Week** | Meetings scheduled per week | 5-10 (SDR), 8-15 (AE) |
| **Talk Time/Day** | Minutes on calls per day | 120-180 min (outbound) |
| **Activity Score** | Weighted sum of all activities | 0-100 scale |

### Conversion Metrics (Process Indicators)
| Metric | Formula | Benchmark |
|--------|---------|-----------|
| **Lead → Meeting** | Meetings / leads contacted | 5-15% (cold), 20-40% (inbound) |
| **Meeting → Proposal** | Proposals / meetings held | 40-60% |
| **Proposal → Close** | Closes / proposals sent | 25-40% |
| **Full Funnel** | Closes / total leads | 2-5% (cold), 10-20% (inbound) |
| **Speed to Lead** | Avg minutes to first response | <5 min = best in class |

### Revenue Metrics (Lagging Indicators)
| Metric | Formula | Benchmark |
|--------|---------|-----------|
| **Revenue/Month** | Total closed revenue | Role-dependent |
| **Avg Deal Size** | Revenue / deals closed | Industry-dependent |
| **Pipeline Value** | Sum of weighted opportunities | 3-5x monthly quota |
| **Pipeline Velocity** | (Deals x Win% x Avg Size) / Cycle Days | Higher = better |
| **Revenue per Activity** | Revenue / total activities | Efficiency measure |

## Instructions

When given sales data, generate:

```
## Rep Performance Report: [Name]
### Period: [Date Range]

---

### SCORECARD

| Category | Metric | Actual | Target | Status |
|----------|--------|--------|--------|--------|
| Activity | Calls/day | XX | XX | [on/above/below] |
| Activity | Emails/day | XX | XX | [on/above/below] |
| Activity | Meetings/week | XX | XX | [on/above/below] |
| Conversion | Lead → Meeting | XX% | XX% | [on/above/below] |
| Conversion | Meeting → Proposal | XX% | XX% | [on/above/below] |
| Conversion | Proposal → Close | XX% | XX% | [on/above/below] |
| Revenue | MTD Revenue | $XX | $XX | [on/above/below] |
| Revenue | Pipeline Value | $XX | $XX | [on/above/below] |
| Revenue | Avg Deal Size | $XX | $XX | [on/above/below] |

### PERFORMANCE GRADE: [A/B/C/D/F]

### TRENDS (vs. Previous Period)
- Activity: [up/down X%] — [interpretation]
- Conversion: [up/down X%] — [interpretation]
- Revenue: [up/down X%] — [interpretation]

### CHURN RISK: [LOW / MEDIUM / HIGH / CRITICAL]
[Explanation of churn risk assessment]

### TOP RECOMMENDATION
[The single highest-leverage action to improve performance]
```

## Churn Risk Scoring

Applies to tracking rep retention risk (for managers) or client churn risk (for account managers).

| Signal | Points | Weight |
|--------|--------|--------|
| Activity down >20% week-over-week | +25 | High |
| Missed quota 2+ consecutive months | +20 | High |
| Response time increasing | +15 | Medium |
| Pipeline not being replenished | +15 | Medium |
| Cancellation language in communications | +30 | Critical |
| Engagement with training/tools declining | +10 | Low |
| Peer performance significantly higher | +10 | Low |

| Score | Risk Level | Action |
|-------|------------|--------|
| 0-20 | LOW | Standard check-in |
| 21-45 | MEDIUM | 1:1 coaching session, identify blockers |
| 46-70 | HIGH | Performance improvement plan, daily check-ins |
| 71-100 | CRITICAL | Immediate intervention, retention conversation |

## Example

### Input
> Solo operator. Last 30 days: 47 cold calls, 156 emails, 8 meetings booked, 5 proposals sent, 2 deals closed. Revenue: $6,500. Pipeline: $22,000 across 6 opportunities. Target: $10,000/month. Previous month: 1 deal closed for $3,200.

### Output

| Category | Metric | Actual | Target | Status |
|----------|--------|--------|--------|--------|
| Activity | Calls/day | 2.1 | 5 | BELOW |
| Activity | Emails/day | 7.1 | 15 | BELOW |
| Activity | Meetings/week | 2 | 3 | BELOW |
| Conversion | Lead → Meeting | 17% | 10% | ABOVE |
| Conversion | Meeting → Proposal | 63% | 50% | ABOVE |
| Conversion | Proposal → Close | 40% | 30% | ABOVE |
| Revenue | MTD Revenue | $6,500 | $10,000 | BELOW |
| Revenue | Pipeline Value | $22,000 | $30,000 | BELOW |
| Revenue | Avg Deal Size | $3,250 | $3,000 | ABOVE |

**PERFORMANCE GRADE: B-**

**TRENDS**: Revenue up 103% MoM. Conversion rates are strong. Activity volume is the bottleneck — not skill.

**CHURN RISK**: N/A (solo operator)

**TOP RECOMMENDATION**: Your conversion rates are elite (40% proposal-to-close is top quartile). The ONLY problem is volume. Increase cold calls from 2/day to 5/day and emails from 7/day to 15/day. At your current conversion rates, that alone puts you at $13K+ next month. Your skill is not the problem — your pipeline is starving.

## Team Leaderboard Mode

For managers tracking multiple reps:

```
| Rank | Rep | Revenue | Close Rate | Activity Score | Trend | Risk |
|------|-----|---------|------------|----------------|-------|------|
| 1 | Sarah | $18,200 | 38% | 92/100 | +12% | LOW |
| 2 | Mike | $14,100 | 31% | 78/100 | +5% | LOW |
| 3 | Alex | $8,400 | 22% | 65/100 | -15% | MEDIUM |
| 4 | Jordan | $3,100 | 12% | 41/100 | -28% | HIGH |
```

---

*Built by [KOINO Capital](https://koino.capital) — Agentic growth systems that run while you sleep.*
*Want this running autonomously 24/7? [Deploy with KOINO](https://koino.capital/deploy)*
