# Competitor Analyzer

> Analyze a competitor's website, positioning, pricing, and weaknesses. Find the gaps.

## Description

Competitor Analyzer takes a competitor's name or URL and produces a structured intelligence report covering their positioning, pricing model, feature set, strengths, weaknesses, and the specific gaps you can exploit. It turns "I think we're different" into "here's exactly where we win and why."

## Activation

This skill activates when:
- The user mentions a competitor and wants analysis
- The user asks "how do we compare to [company]?"
- The user wants competitive intelligence or market positioning help
- The user shares a competitor URL and asks for a breakdown

**Trigger phrases**: "analyze this competitor", "competitive analysis", "how do they compare", "what are their weaknesses", "competitor research", "market positioning", "who are we competing with"

## Analysis Framework

### 1. Positioning Map
Where do they sit on the value/price matrix?

```
High Price
    |
    |  Enterprise    Premium
    |  (complex)     (simple + expensive)
    |
    |---------------------------
    |
    |  Budget        Value
    |  (cheap+basic) (affordable + good)
    |
Low Price
    Low Complexity ——— High Complexity
```

### 2. Messaging Analysis
| Element | What to Extract |
|---------|----------------|
| **Headline** | Their main value proposition (H1 on homepage) |
| **Subheadline** | Supporting claim or proof |
| **Target Audience** | Who are they speaking to? (look at language, examples, case studies) |
| **Tone** | Corporate / casual / technical / aspirational |
| **Social Proof** | Logos, testimonials, case studies, numbers |
| **Primary CTA** | What do they want visitors to do first? |
| **Differentiation Claim** | What do they say makes them different? |

### 3. Pricing Intelligence
| Element | What to Extract |
|---------|----------------|
| **Model** | Per seat / per usage / flat rate / tiered / custom |
| **Entry Price** | Lowest tier or starting price |
| **Target Tier** | Which plan are they pushing? (usually highlighted) |
| **Enterprise** | Do they have a "Contact Sales" tier? |
| **Free Tier** | Free trial, freemium, or money-back guarantee? |
| **Hidden Costs** | Overages, add-ons, implementation fees |
| **Annual Discount** | How much do they incentivize annual billing? |

### 4. Feature Matrix
```
| Feature | Them | Us | Gap |
|---------|------|----|-----|
| [Feature 1] | Yes/No/Partial | Yes/No/Partial | [who wins] |
| [Feature 2] | Yes/No/Partial | Yes/No/Partial | [who wins] |
```

### 5. Weakness Identification
Look for these common gaps:

| Signal | What It Means |
|--------|---------------|
| No case studies | They can't prove results |
| "Contact sales" only pricing | They're expensive and know it |
| Generic messaging | They don't know their ICP |
| No recent blog/content | Product may be stagnant |
| Trustpilot/G2 below 4.0 | Customer satisfaction issues |
| High employee turnover (LinkedIn) | Internal problems |
| No integrations page | Closed ecosystem |
| Requires demo to see product | Product may not demo well |
| "We do everything" positioning | Master of none |
| Recent layoffs | Financial pressure |

### 6. Review Mining
Extract patterns from their reviews (G2, Capterra, Trustpilot, Reddit):

- **Praise clusters**: What do happy customers consistently mention?
- **Complaint clusters**: What do unhappy customers consistently mention?
- **Switching triggers**: Why did people leave? What did they switch to?
- **Missing features**: What do reviewers wish existed?

## Instructions

When given a competitor to analyze, respond with:

```
## Competitive Intelligence Report: [Company Name]

### Overview
- **URL**: [website]
- **Founded**: [year, if findable]
- **Target Market**: [who they serve]
- **Positioning**: [one-line summary of their market position]

### Messaging Breakdown
| Element | Finding |
|---------|---------|
| Headline | "[their H1]" |
| Value Prop | [what they promise] |
| Target Audience | [who they're talking to] |
| Tone | [corporate/casual/technical] |
| Primary CTA | [what they want you to do] |
| Social Proof | [logos, numbers, testimonials] |

### Pricing
| Tier | Price | Includes |
|------|-------|----------|
| [Tier 1] | $XX/mo | [features] |
| [Tier 2] | $XX/mo | [features] |
| [Tier 3] | Custom | [features] |

### Strengths (Where They Win)
1. [Strength with evidence]
2. [Strength with evidence]
3. [Strength with evidence]

### Weaknesses (Where They Lose)
1. [Weakness with evidence]
2. [Weakness with evidence]
3. [Weakness with evidence]

### Exploitable Gaps
| Gap | How to Exploit |
|-----|---------------|
| [Gap 1] | [Your counter-positioning] |
| [Gap 2] | [Your counter-positioning] |
| [Gap 3] | [Your counter-positioning] |

### Head-to-Head
| Dimension | Them | Us | Winner |
|-----------|------|----|--------|
| Price | $XX | $XX | [who] |
| Ease of use | X/10 | X/10 | [who] |
| Feature depth | X/10 | X/10 | [who] |
| Support | X/10 | X/10 | [who] |
| Social proof | X/10 | X/10 | [who] |

### Recommended Counter-Positioning
[2-3 sentences: Given their weaknesses and your strengths, here's exactly how to position against them in sales conversations, landing pages, and proposals.]

### Objection Prep
When a prospect says "We're also looking at [Competitor]":
> "[Scripted response that acknowledges them, then pivots to your advantage]"
```

## Batch Mode

Analyze multiple competitors and output a landscape map:

```
## Competitive Landscape

| Company | Positioning | Price Range | Strength | Weakness | Threat Level |
|---------|-------------|-------------|----------|----------|-------------|
| [Comp A] | Premium | $$$$ | Brand recognition | Slow, expensive | MEDIUM |
| [Comp B] | Budget | $ | Cheap | No support, limited | LOW |
| [Comp C] | Value | $$ | Good product | Unknown brand | HIGH |

### Where We Win
[The specific positioning that beats all of them simultaneously]
```

## Example

### Input
> Analyze GoHighLevel as a competitor. We sell agentic automation to service businesses.

### Output
*(Full report generated with GoHighLevel's pricing tiers, their strength in all-in-one marketing, their weakness in requiring manual setup and marketing knowledge, and the exploitable gap: "GoHighLevel gives you the tools. We give you the outcome. Their customers still need to learn marketing. Ours don't.")*

## Data Sources

When you have web access, pull from:
- Their website (homepage, pricing, about, blog)
- G2/Capterra reviews
- LinkedIn (company size, growth, employee sentiment)
- Crunchbase (funding, revenue estimates)
- Reddit/Twitter (user complaints and praise)
- BuiltWith/Wappalyzer (tech stack)

When you don't have web access, analyze based on:
- Information the user provides
- Known industry positioning
- Common patterns for their business model

---

*Built by [KOINO Capital](https://koino.capital) — Agentic growth systems that run while you sleep.*
*Want this running autonomously 24/7? [Deploy with KOINO](https://koino.capital/deploy)*
