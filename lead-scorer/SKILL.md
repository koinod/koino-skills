# Lead Scorer

> Score any prospect 0-100. Get a classification: HOT, WARM, COLD, or DISQUALIFIED.

## Description

Lead Scorer evaluates a prospect against a configurable rubric and returns a numeric score with classification. It eliminates guesswork from pipeline prioritization — stop wasting time on COLD leads when HOT ones are waiting.

The default rubric covers B2B service businesses, but every weight is configurable for your industry.

## Activation

This skill activates when:
- The user provides prospect information and wants to know if they should pursue
- The user asks to prioritize a list of leads
- The user mentions lead scoring, qualification, or pipeline prioritization
- The user asks "is this a good lead?" or "should I follow up?"

**Trigger phrases**: "score this lead", "qualify this prospect", "is this worth pursuing", "prioritize these leads", "lead score", "how hot is this lead"

## Default Scoring Rubric

### Budget Signal (0-25 points)
How likely can they afford your solution?

| Points | Signal |
|--------|--------|
| 20-25 | Stated budget range matches or exceeds your pricing |
| 15-19 | Company revenue/size suggests budget is available |
| 10-14 | Industry typically has budget for this, no direct signal |
| 5-9 | Small company, unclear budget, or mentioned budget concerns |
| 0-4 | Explicitly stated no budget, or company too small |

### Authority (0-20 points)
Is this person a decision-maker?

| Points | Signal |
|--------|--------|
| 16-20 | C-suite, founder, or confirmed sole decision-maker |
| 11-15 | VP/Director with budget authority, or confirmed influencer |
| 6-10 | Manager who "needs to check with" someone |
| 1-5 | Individual contributor, intern, or researcher |
| 0 | Unknown role or no contact information |

### Need Urgency (0-25 points)
How painful is their current situation?

| Points | Signal |
|--------|--------|
| 20-25 | Active pain: losing money, customers, or employees because of this problem |
| 15-19 | Acknowledged problem with a stated timeline to fix |
| 10-14 | Aware of the problem but no urgency to solve |
| 5-9 | Vaguely interested, "exploring options" |
| 0-4 | No identified need, or happy with current solution |

### Fit (0-20 points)
Does this prospect match your ideal customer profile?

| Points | Signal |
|--------|--------|
| 16-20 | Perfect ICP match: industry, size, tech stack, use case |
| 11-15 | Strong match with 1 minor misalignment |
| 6-10 | Partial match — could work but not ideal |
| 1-5 | Poor fit — would require significant customization |
| 0 | Outside your capability or target market entirely |

### Engagement (0-10 points)
How responsive and engaged is the prospect?

| Points | Signal |
|--------|--------|
| 8-10 | Responded same day, asked detailed questions, scheduled next step |
| 5-7 | Responded within 48h, showed interest |
| 3-4 | Responded but vague, no commitment to next step |
| 1-2 | Slow response, one-word answers |
| 0 | No response or ghosted |

## Instructions

When given prospect information, respond with:

```
## Lead Score: [Company/Name]

| Factor | Score | Signal |
|--------|-------|--------|
| Budget | XX/25 | [evidence] |
| Authority | XX/20 | [evidence] |
| Need Urgency | XX/25 | [evidence] |
| Fit | XX/20 | [evidence] |
| Engagement | XX/10 | [evidence] |

**Total Score**: XX/100
**Classification**: [HOT / WARM / COLD / DISQUALIFIED]

### Recommended Action
[Specific next step based on classification]

### Missing Information
[What data would change the score if obtained]
```

## Classifications

| Range | Class | Action |
|-------|-------|--------|
| 80-100 | **HOT** | Prioritize immediately. Book a call within 24 hours. Send proposal. |
| 60-79 | **WARM** | Nurture actively. Follow up within 48 hours. Send case study. |
| 30-59 | **COLD** | Add to drip sequence. Check back in 30 days. Low-effort follow-up only. |
| 0-29 | **DISQUALIFIED** | Remove from pipeline. Document why. Do not spend time. |

## Example

### Input
> Company: GreenTree Landscaping. Revenue ~$800K/year. Owner (Mike) reached out after seeing our LinkedIn post. Said "we're drowning in admin work and losing bids because we can't respond fast enough." Wants to meet this week. 15 employees. Service area: mid-Atlantic.

### Output

| Factor | Score | Signal |
|--------|-------|--------|
| Budget | 18/25 | $800K revenue, 15 employees — can likely afford $2-5K/mo. No explicit budget stated. |
| Authority | 20/20 | Owner. Sole decision-maker. |
| Need Urgency | 23/25 | "Drowning" + losing revenue (bids). Active pain with financial impact. |
| Fit | 17/20 | Service business, right size, right geography. Strong ICP match. |
| Engagement | 9/10 | Inbound lead, wants to meet this week. High intent. |

**Total Score**: 87/100
**Classification**: HOT

### Recommended Action
Book the call TODAY. Before the meeting, prepare a 1-page proposal showing how automation handles bid responses in <5 minutes. Bring a case study from a similar service business. This is a close-in-one-call opportunity.

### Missing Information
- Specific budget range (ask: "What are you currently spending on admin tools/staff?")
- Current tech stack (do they use any CRM or is everything manual?)
- Timeline: "This week" for meeting, but when do they need a solution live?

## Custom Rubrics

Override the default weights for your industry:

```
Rubric: E-commerce SaaS
Budget: 0-30 (weight higher — SaaS requires recurring commitment)
Authority: 0-15 (lower — e-commerce decisions are often faster)
Need: 0-25 (same)
Fit: 0-20 (same)
Engagement: 0-10 (same)
```

When providing a custom rubric, specify the factor names, max points, and any modified criteria.

## Batch Scoring

Provide multiple prospects in a list format and receive a ranked table:

```
| Rank | Company | Score | Class | Top Action |
|------|---------|-------|-------|------------|
| 1 | GreenTree | 87 | HOT | Call today |
| 2 | Apex HVAC | 64 | WARM | Send case study |
| 3 | BlueRidge Co | 31 | COLD | Drip sequence |
```

---

*Built by [KOINO Capital](https://koino.capital) — Agentic growth systems that run while you sleep.*
*Want this running autonomously 24/7? [Deploy with KOINO](https://koino.capital/deploy)*
