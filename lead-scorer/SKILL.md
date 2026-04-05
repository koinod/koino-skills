---
name: lead-scorer
description: Score and prioritize your leads with AI
version: 1.0.0
author: KOINO Capital
license: MIT
tags: [sales, leads, scoring, crm, prioritization, pipeline]
---

# AI Lead Scorer

Score any lead 0-100 and get a clear action plan. Stop guessing which leads to call first -- let data and pattern matching decide.

## Usage

Provide lead information in any format. The more you provide, the better the score:

### Required Fields

| Field | Example |
|-------|---------|
| **Lead Name** | "Marcus Webb" |
| **Company** | "TerraForce Industrial" |
| **Source** | "Inbound -- downloaded pricing PDF" |

### Optional Fields (improve accuracy)

| Field | Example |
|-------|---------|
| **Title/Role** | "Director of Operations" |
| **Company Size** | "85 employees, ~$12M revenue" |
| **Industry** | "Industrial equipment manufacturing" |
| **Interaction History** | "Opened 3 emails, attended webinar, asked about pricing" |
| **Budget Signals** | "Mentioned Q2 budget approval" |
| **Timeline** | "Looking to implement by June" |
| **Pain Points** | "Current system requires manual data entry across 4 platforms" |
| **Competition** | "Currently evaluating us and 2 competitors" |
| **Notes** | "Referred by existing client. Seemed frustrated with current vendor." |

---

## Scoring Framework

### Category Weights (default)

| Category | Weight | What It Measures |
|----------|--------|-----------------|
| **Fit** | 30% | How well do they match your ideal customer? |
| **Intent** | 25% | How much buying behavior have they shown? |
| **Authority** | 20% | Can this person actually make or influence the decision? |
| **Timing** | 15% | Is there urgency or a deadline driving them? |
| **Engagement** | 10% | How actively are they interacting with you? |

You can customize these weights. Just specify your preferred weights and they'll be applied.

### Fit Score (0-30 points)

| Signal | Points |
|--------|--------|
| Company size matches ICP | +5-10 |
| Industry is in your sweet spot | +5-10 |
| They have the problem you solve | +5-10 |
| Geography/market alignment | +2-5 |
| Tech stack compatibility (if relevant) | +2-5 |
| Revenue range matches your pricing | +3-5 |

**Deductions:**
| Signal | Points |
|--------|--------|
| Company too small for your pricing | -5 to -10 |
| Industry you've never served | -3 to -5 |
| No clear problem match | -5 to -10 |

### Intent Score (0-25 points)

| Signal | Points |
|--------|--------|
| Requested pricing/proposal | +10-15 |
| Mentioned specific timeline | +5-10 |
| Compared you to competitors (means they're shopping) | +5-8 |
| Asked detailed product/service questions | +5-8 |
| Downloaded bottom-of-funnel content | +3-5 |
| Visited pricing page (if tracked) | +3-5 |
| Mentioned budget availability | +5-10 |

**Deductions:**
| Signal | Points |
|--------|--------|
| "Just researching" with no timeline | -5 to -10 |
| Only engaged with top-of-funnel content | -3 to -5 |
| Ghosted after initial contact | -5 to -8 |

### Authority Score (0-20 points)

| Signal | Points |
|--------|--------|
| C-suite or business owner | +15-20 |
| VP or Director level | +10-15 |
| Manager with budget authority | +8-12 |
| Individual contributor (but champion) | +5-8 |
| Explicitly said "I make this decision" | +5 bonus |
| Mentioned needing board/committee approval | -3 to -5 |
| Intern or junior role | -5 to -10 |

### Timing Score (0-15 points)

| Signal | Points |
|--------|--------|
| Actively in buying process NOW | +12-15 |
| Deadline mentioned (contract renewal, fiscal year, event) | +8-12 |
| "Next quarter" | +5-8 |
| "Sometime this year" | +3-5 |
| No timeline mentioned | +1-2 |
| "Maybe next year" | 0 |

### Engagement Score (0-10 points)

| Signal | Points |
|--------|--------|
| Responded within 24 hours | +3-5 |
| Multiple touchpoints (email + call + event) | +3-5 |
| Referred by existing customer | +5 (max) |
| Engaged with 3+ pieces of content | +2-4 |
| Single interaction only | +1-2 |
| Has not responded to outreach | 0-1 |

---

## Output Format

For each lead, deliver:

### 1. Score Summary

```
LEAD: [Name] at [Company]
SCORE: [X]/100
CATEGORY: [HOT / WARM / COLD]
CONFIDENCE: [HIGH / MEDIUM / LOW] (based on how much info was provided)
```

**Category thresholds:**
- **HOT (75-100)**: Contact within 24 hours. High fit, strong intent, decision-maker, urgent timeline.
- **WARM (40-74)**: Nurture actively. Good potential but missing one or more key signals.
- **COLD (0-39)**: Low priority. Add to nurture sequence but don't spend active selling time.

### 2. Score Breakdown

```
Fit:        [X]/30  -- [1-sentence explanation]
Intent:     [X]/25  -- [1-sentence explanation]
Authority:  [X]/20  -- [1-sentence explanation]
Timing:     [X]/15  -- [1-sentence explanation]
Engagement: [X]/10  -- [1-sentence explanation]
```

### 3. Key Signals

List the top 3 positive signals and top 3 risk factors:

**Positive:**
- [Signal 1]
- [Signal 2]
- [Signal 3]

**Risk Factors:**
- [Risk 1]
- [Risk 2]
- [Risk 3]

### 4. Action Brief

Based on the score, provide a specific action plan:

**For HOT leads:**
- Recommended next step (specific, not generic)
- Talking points tailored to their pain points
- Potential objections to prepare for
- Suggested timeline for follow-up

**For WARM leads:**
- What information is missing that would upgrade them to HOT
- Specific nurture actions (content to send, questions to ask)
- Trigger events to watch for
- Re-score date recommendation

**For COLD leads:**
- Why they scored low (honest assessment)
- Whether they're worth keeping in the pipeline at all
- Automated nurture recommendation
- Conditions that would trigger re-evaluation

---

## Batch Scoring

You can score multiple leads at once. Provide a list and receive:

1. Individual scores for each lead
2. A **priority ranking** (sorted by score, descending)
3. A **pipeline summary**:
   - Total leads scored
   - HOT / WARM / COLD distribution
   - Average score
   - Top 3 leads to contact TODAY

---

## Customization

### Custom ICP Definition

If you provide your Ideal Customer Profile, scoring becomes dramatically more accurate:

```
My ICP:
- Industry: [e.g., "B2B SaaS, $5M-$50M ARR"]
- Company size: [e.g., "50-500 employees"]
- Decision maker: [e.g., "VP Sales or CRO"]
- Budget range: [e.g., "$2K-$10K/month"]
- Key pain: [e.g., "Manual reporting takes 20+ hours/week"]
- Disqualifiers: [e.g., "Under $1M revenue, no dedicated sales team"]
```

### Custom Weight Adjustment

Override default weights for your sales motion:

- **High-ticket enterprise**: Increase Authority to 30%, reduce Engagement to 5%
- **Self-serve product**: Increase Intent to 35%, reduce Authority to 10%
- **Referral-heavy business**: Increase Engagement to 20%, reduce Timing to 10%

---

## Scoring Accuracy Tips

1. **More data = better scores.** A lead with just a name and company will get a LOW confidence score. That's honest, not a bug.
2. **Re-score after new interactions.** A WARM lead who requests pricing should be re-scored immediately.
3. **Calibrate to your close rate.** If your HOT leads aren't closing at 30%+, your scoring weights need adjustment.
4. **Don't ignore COLD leads entirely.** 10% of today's COLD leads become next quarter's HOT leads. Automate nurture, don't delete.
5. **Trust the risks section.** If the score is high but the risks are serious, investigate before investing heavy time.

---

*Powered by [KOINO Capital](https://koino.capital) -- AI systems that fill your pipeline and close your deals.*
