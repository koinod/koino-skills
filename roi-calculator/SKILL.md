---
name: roi-calculator
description: Calculate the ROI of AI automation for your business
version: 1.0.0
author: KOINO Capital
license: MIT
tags: [roi, automation, calculator, ai, business-case, savings]
---

# AI Automation ROI Calculator

Get a concrete dollars-and-cents estimate of what AI automation would save your business. No fluff, no inflated projections -- just math you can take to your team, your partner, or your bank account.

## Usage

Provide the following:

### Required Inputs

| Field | Example | Notes |
|-------|---------|-------|
| **Industry** | "Digital marketing agency" | Helps benchmark against similar businesses |
| **Team Size** | 8 | Total people (including you) |
| **Manual Hours per Week** | 35 | Total hours your team spends on repetitive tasks |
| **Average Hourly Cost** | $45 | Loaded cost (salary + benefits + overhead / hours) |

### Optional Inputs (improve accuracy)

| Field | Example | Notes |
|-------|---------|-------|
| **Annual Revenue** | $1.2M | Used for revenue-impact calculations |
| **Top 3 Time Sinks** | "Reporting, client emails, invoice creation" | Get specific automation estimates |
| **Current Tool Spend** | $2,400/month | Factor in tools that automation might replace |
| **Growth Target** | "Double revenue without adding headcount" | Changes the framing of ROI |
| **Error/Rework Rate** | "~10% of deliverables need rework" | Hidden cost most businesses ignore |

---

## Calculation Engine

### Step 1: Baseline Cost Analysis

```
CURRENT STATE:
  Manual hours/week:              [X] hours
  Team members involved:          [X] people
  Avg hourly cost (loaded):       $[X]/hour
  Weekly cost of manual work:     $[hours x cost]
  Annual cost of manual work:     $[weekly x 50 weeks]
```

**Loaded hourly cost guide** (if they don't know):
- For employees: (Annual salary x 1.3) / 2,080 hours
  - The 1.3 multiplier accounts for benefits, taxes, office costs
- For the business owner: Use your target hourly rate, or revenue / hours worked
- For contractors: Their rate is already loaded

### Step 2: Automation Savings Estimate

Not all manual hours can be automated. Apply realistic automation rates by task type:

| Task Category | Automation Rate | Examples |
|---------------|----------------|---------|
| **Data entry & transfer** | 85-95% | CRM updates, spreadsheet population, cross-system data sync |
| **Report generation** | 75-90% | Weekly reports, dashboards, client updates |
| **Email & communication** | 50-70% | Follow-ups, templates, meeting scheduling, auto-responses |
| **Content creation** | 40-60% | Social posts, email drafts, basic copywriting |
| **Client onboarding** | 60-80% | Welcome sequences, form processing, account setup |
| **Invoicing & billing** | 80-95% | Invoice creation, payment reminders, expense tracking |
| **Scheduling & coordination** | 70-85% | Calendar management, resource allocation, task assignment |
| **Quality assurance** | 30-50% | Review checklists, error detection, compliance checks |
| **Research & analysis** | 40-60% | Market research, competitor monitoring, data analysis |
| **Customer support** | 40-65% | FAQ responses, ticket routing, status updates |

**Conservative estimate**: Use the LOW end of each range
**Realistic estimate**: Use the MIDPOINT
**Aggressive estimate**: Use the HIGH end (only if you have strong technical execution)

```
AUTOMATION POTENTIAL:
  Total manual hours/week:          [X]
  Automatable hours (conservative): [X] ([Y]%)
  Automatable hours (realistic):    [X] ([Y]%)
  Automatable hours (aggressive):   [X] ([Y]%)
```

### Step 3: Financial Impact

```
ANNUAL SAVINGS (using realistic estimate):

  Direct labor savings:
    [Automatable hours] x $[hourly cost] x 50 weeks = $[X]/year

  Error reduction savings:
    [Rework rate] x [total project hours] x $[hourly cost] x 50% reduction = $[X]/year

  Tool consolidation savings:
    [Tools replaced] x $[monthly cost] x 12 = $[X]/year

  Speed-to-revenue improvement:
    [Faster delivery/response] → estimated [X]% improvement in close rate
    [Current revenue] x [improvement %] = $[X]/year potential

  ─────────────────────────────────
  TOTAL ESTIMATED ANNUAL SAVINGS:    $[X]
  TOTAL ESTIMATED ANNUAL SAVINGS:    $[X] (conservative)
  TOTAL ESTIMATED ANNUAL SAVINGS:    $[X] (aggressive)
```

### Step 4: Implementation Cost Estimate

```
IMPLEMENTATION COSTS:

  Automation tools/platforms:       $[X]/month → $[X]/year
  Setup & configuration:            $[X] (one-time)
  Training & transition:            $[X] (one-time, usually 2-4 weeks of reduced productivity)
  Ongoing maintenance:              $[X]/month → $[X]/year

  ─────────────────────────────────
  YEAR 1 TOTAL COST:                $[X]
  YEAR 2+ ANNUAL COST:              $[X]
```

**Tool cost benchmarks by business size:**

| Team Size | Typical Monthly Tool Cost | What It Covers |
|-----------|--------------------------|----------------|
| 1-3 | $50-$200/mo | Zapier/Make, email tool, basic CRM |
| 4-10 | $200-$800/mo | CRM, automation platform, AI tools, integrations |
| 11-25 | $800-$2,500/mo | Enterprise CRM, custom automations, AI agents, dashboards |
| 25-100 | $2,500-$10,000/mo | Full stack, custom development, dedicated support |

### Step 5: ROI Summary

```
ROI SUMMARY:
  ═══════════════════════════════════════════════
  Annual savings (realistic):       $[X]
  Year 1 implementation cost:       $[X]
  ─────────────────────────────────
  NET YEAR 1 SAVINGS:               $[X]
  YEAR 2+ ANNUAL NET SAVINGS:       $[X]

  PAYBACK PERIOD:                   [X] months
  3-YEAR ROI:                       [X]%
  HOURS RETURNED TO YOUR TEAM:      [X] hours/year
  ═══════════════════════════════════════════════
```

**Payback period formula:**
Total implementation cost / (Monthly savings - Monthly tool cost) = Months to payback

**3-Year ROI formula:**
((3-year savings - 3-year costs) / 3-year costs) x 100 = ROI %

---

## Step 6: Recommended Automations

Based on the industry and time sinks provided, recommend the **top 5 specific automations** to implement:

For each:

```
#[Rank]: [Automation Name]
Hours Saved: [X]/week
Annual Value: $[X]
Difficulty: [EASY / MEDIUM / HARD]
Tools Needed: [Tool 1, Tool 2]
Free Option: [Free alternative if budget is tight]

What It Does:
[2-3 sentences explaining exactly what gets automated and how]

Implementation:
[1-2 sentences on how to set this up]
```

---

## Step 7: The Opportunity Cost Frame

Most businesses only think about savings. The bigger number is what you could DO with the reclaimed time:

```
OPPORTUNITY COST ANALYSIS:

  Hours freed per week:             [X]
  That's equivalent to:             [X] full-time employees
  
  What you could do with that time:
  - Close [X] more deals/month (at current close rate)
  - Create [X] more content pieces/week
  - Onboard [X] more clients/month
  - Reduce delivery time by [X]%
  
  If you redirected 50% of freed hours to revenue generation:
  [Hours] x $[revenue per hour] x 50 weeks = $[X] additional revenue potential
```

---

## Industry Benchmarks

For reference, here are typical automation results by industry:

| Industry | Avg Hours Saved/Week | Avg Annual Savings | Typical Payback |
|----------|---------------------|-------------------|-----------------|
| Marketing Agency | 25-40 hrs | $65K-$150K | 2-4 months |
| Real Estate | 15-25 hrs | $40K-$80K | 1-3 months |
| E-commerce | 20-35 hrs | $50K-$120K | 2-4 months |
| Professional Services | 15-30 hrs | $60K-$140K | 2-5 months |
| SaaS Company | 20-40 hrs | $80K-$200K | 3-6 months |
| Construction/Trades | 10-20 hrs | $30K-$70K | 1-3 months |
| Healthcare Practice | 15-25 hrs | $50K-$100K | 2-4 months |
| Financial Services | 20-35 hrs | $80K-$180K | 3-6 months |

*These are based on teams of 5-20 people. Adjust proportionally for your team size.*

---

## What This Calculator Does NOT Account For

Be honest about what the numbers miss:

1. **Transition costs**: There's a productivity dip during implementation (usually 2-4 weeks)
2. **Learning curve**: Your team needs time to adopt new tools
3. **Edge cases**: Automations handle 80% of cases well; the other 20% still needs humans
4. **Maintenance**: Automations break when APIs change, tools update, or processes evolve
5. **Compound effects**: The calculator is LINEAR, but real automation benefits COMPOUND -- year 2 savings are usually 30-50% higher than year 1

---

## Next Steps

Your ROI estimate is done. Here's what to do with it:

1. **If payback period is under 6 months** -- this is a no-brainer. Start with automation #1 this week.
2. **If payback period is 6-12 months** -- start with the quick wins (EASY difficulty items) to build momentum.
3. **If payback period is 12+ months** -- you may need to focus on higher-impact areas or reduce implementation costs.

**Want the full audit with implementation?**
We've done this for dozens of businesses. We'll audit your workflows, build the automations, and guarantee measurable results.

**Book your full audit at [koino.capital/audit](https://koino.capital/audit)**

---

*Powered by [KOINO Capital](https://koino.capital) -- we don't just calculate ROI, we deliver it.*
