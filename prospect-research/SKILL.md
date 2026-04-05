# Prospect Research

> Research any company and generate a structured intelligence profile in 60 seconds.

---
name: prospect-research
version: 1.0.0
description: Research any company and generate a structured intelligence profile
author: KOINO Capital
tags: [sales, research, prospecting]
---

## Description

Prospect Research takes a company name and produces a full intelligence dossier — industry, team size, services, tech stack, funding, recent news, and strategic angles. Everything a seller needs before the first call, generated in under a minute.

Stop spending 20 minutes per prospect on LinkedIn and Crunchbase. This skill does the homework so you can focus on the conversation.

## Activation

This skill activates when:
- The user wants to research a company before a sales call
- The user provides a company name and wants an intelligence profile
- The user asks for a prospect dossier, company research, or pre-call prep
- The user mentions "research", "profile", "look up", or "what do we know about"

**Trigger phrases**: "research this company", "prospect research", "look up", "company profile", "pre-call research", "tell me about [company]", "dossier on"

## Instructions

When the user provides a company name (and optionally a URL, contact name, or industry hint):

### Step 1: Gather Intelligence

Use web search to find:
- **Company website** — homepage, about page, team page, careers page, blog
- **LinkedIn** — company page, employee count, recent posts
- **Crunchbase / PitchBook** — funding, investors, revenue estimates
- **News** — press releases, articles, mentions from last 90 days
- **Tech stack clues** — job postings (what tools they hire for), BuiltWith data, integrations mentioned
- **Social presence** — Twitter/X, YouTube, podcast appearances
- **Reviews** — G2, Glassdoor, Google Reviews if B2C

### Step 2: Generate the Profile

Output the following structured markdown:

```markdown
# [Company Name] — Prospect Intelligence Profile

**Generated**: [date]
**Confidence Level**: [High / Medium / Low] (based on data availability)

---

## Company Overview
| Field | Detail |
|-------|--------|
| **Full Name** | [Legal name if found] |
| **Website** | [URL] |
| **Industry** | [Primary industry + sub-segment] |
| **Founded** | [Year] |
| **Headquarters** | [City, State/Country] |
| **Team Size** | [Estimate with source — LinkedIn, careers page, etc.] |
| **Revenue Estimate** | [Range if available] |
| **Funding** | [Total raised, last round, investors] |
| **Business Model** | [B2B / B2C / B2B2C, SaaS / Services / Product, etc.] |

## What They Do
[2-3 sentence plain-English summary. No jargon. What problem do they solve, for whom?]

## Products & Services
- [Product/service 1] — [one-line description]
- [Product/service 2] — [one-line description]
- [etc.]

## Tech Stack (observed or inferred)
| Category | Tools |
|----------|-------|
| **CRM** | [e.g., Salesforce, HubSpot] |
| **Marketing** | [e.g., Marketo, Mailchimp] |
| **Engineering** | [e.g., React, AWS, Python] |
| **Analytics** | [e.g., Mixpanel, GA4] |
| **Other** | [Anything notable] |

*Sources: job postings, integrations page, BuiltWith, etc.*

## Key People
| Name | Title | Notes |
|------|-------|-------|
| [Name] | [Title] | [Relevant detail — LinkedIn post, podcast appearance, quote] |

## Recent News & Activity (last 90 days)
- [Date] — [Headline + 1-sentence summary + source link]
- [Date] — [Headline + 1-sentence summary + source link]
- [Date] — [Headline + 1-sentence summary + source link]

## Strategic Angles (for outreach)

### Pain Points (likely)
1. [Inferred pain point based on industry + company stage + hiring patterns]
2. [Second pain point]
3. [Third pain point]

### Conversation Starters
- "[Reference to recent news or LinkedIn post] — how is that affecting [X]?"
- "[Industry trend] is hitting companies your size hard. How are you handling [specific aspect]?"
- "[Competitor] just [did something]. Does that change anything for your team?"

### Timing Signals
- [Are they hiring? (growth mode)]
- [Did they just raise? (spending mode)]
- [Leadership change? (new priorities)]
- [Negative reviews? (pain is public)]

## Competitive Landscape
| Competitor | How They Differ |
|------------|----------------|
| [Competitor 1] | [Key differentiator] |
| [Competitor 2] | [Key differentiator] |

## Pre-Call Checklist
- [ ] Review their LinkedIn company page
- [ ] Check the contact's recent LinkedIn posts
- [ ] Identify one specific thing to reference in opening
- [ ] Prepare 2-3 questions based on pain points above
- [ ] Have a relevant case study ready
```

### Step 3: Confidence Assessment

Rate the profile:
- **High confidence**: Multiple corroborating sources, recent data, clear picture
- **Medium confidence**: Some gaps, older data, reasonable inferences
- **Low confidence**: Limited public data, heavy inference, flag what's uncertain

## Rules

1. **Cite sources.** Every claim should trace to a URL or observable fact.
2. **Flag uncertainty.** If something is inferred vs. confirmed, say so.
3. **No hallucinated data.** If you can't find revenue, say "Not publicly available" — don't guess a number.
4. **Recency matters.** Deprioritize information older than 12 months unless foundational.
5. **Actionable over comprehensive.** The "Strategic Angles" section is the most valuable part. Spend the most effort there.
6. **Plain English.** Write like a smart colleague briefing you before a meeting, not like a database dump.

## Example

### Input
> Research Gong.io

### Output
*(Full profile following the template above, with real data from web search)*

## Batch Mode

Provide a list of companies to get profiles for each:

```
1. Gong.io
2. Outreach.io
3. Apollo.io
```

Each profile will be generated individually with company-specific research — not templated guesses.

---

*Generated by [KOINO Capital](https://koino.capital) | Full AI readiness analysis: [koino.capital/score](https://koino.capital/score)*
*Want prospect research running on autopilot? [Deploy with KOINO](https://koino.capital/deploy)*
