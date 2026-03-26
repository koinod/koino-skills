# Content QA Scorer

> Score any piece of content on 7 dimensions. Get a verdict: PASS, NEEDS WORK, or KILL.

## Description

Content QA Scorer evaluates written content (social posts, emails, blog articles, ad copy, video scripts) against 7 battle-tested dimensions. Each dimension is scored 1-10 with specific feedback. The final verdict prevents you from publishing mediocre content that damages your brand.

This is not subjective — each dimension has concrete criteria. A score of 6 on "Hook" means something specific and actionable.

## Activation

This skill activates when:
- The user asks to review, score, or QA a piece of content
- The user shares draft content and asks "is this good?"
- The user wants feedback on copy, posts, scripts, or emails
- The user mentions content quality, scoring, or grading

**Trigger phrases**: "score this", "review this content", "is this good", "QA this", "rate this post", "content feedback", "grade this"

## The 7 Dimensions

### 1. Hook (Weight: 2x)
Does the first line stop the scroll? Would someone reading this in a feed of 1000 posts pause on yours?

| Score | Criteria |
|-------|----------|
| 9-10 | Pattern interrupt. Creates an open loop the reader MUST close. |
| 7-8 | Strong curiosity or bold claim. Most people would pause. |
| 5-6 | Decent but predictable. "5 Tips for..." territory. |
| 3-4 | Boring. Reads like every other post in the niche. |
| 1-2 | No hook at all. Starts with context nobody asked for. |

### 2. Value Density
Is every sentence earning its place? Could you cut 30% without losing meaning?

| Score | Criteria |
|-------|----------|
| 9-10 | Every sentence teaches, provokes, or moves the reader. Zero filler. |
| 7-8 | Tight with 1-2 sentences that could be cut. |
| 5-6 | Some filler, some repetition. Could be 30% shorter. |
| 3-4 | More filler than substance. Reader skims. |
| 1-2 | Fluff piece. Says nothing in many words. |

### 3. Brand Alignment
Does this sound like the brand? Could a reader identify who wrote this without seeing the name?

| Score | Criteria |
|-------|----------|
| 9-10 | Unmistakably on-brand. Voice, tone, values all aligned. |
| 7-8 | Mostly on-brand with minor voice inconsistencies. |
| 5-6 | Generic. Could be anyone's content. |
| 3-4 | Off-brand in tone or message. |
| 1-2 | Contradicts brand positioning or values. |

### 4. Engagement Potential
Will people comment, share, save, or DM about this?

| Score | Criteria |
|-------|----------|
| 9-10 | Polarizing, relatable, or so valuable people tag friends. |
| 7-8 | Will generate meaningful comments from target audience. |
| 5-6 | Might get likes but no comments or shares. |
| 3-4 | Passive consumption. Scroll past and forget. |
| 1-2 | Actively boring. Might cause unfollows. |

### 5. CTA Clarity
Is there a clear next step? Does the reader know what to do after consuming this?

| Score | Criteria |
|-------|----------|
| 9-10 | CTA feels natural, specific, and low-friction. |
| 7-8 | Clear CTA but could be more compelling. |
| 5-6 | CTA exists but is vague ("link in bio"). |
| 3-4 | No clear CTA. Reader finishes and does nothing. |
| 1-2 | Multiple competing CTAs or completely missing. |

### 6. Visual/Format
Is the content formatted for the platform? Easy to scan? Proper spacing?

| Score | Criteria |
|-------|----------|
| 9-10 | Perfect for platform. White space, line breaks, formatting all optimized. |
| 7-8 | Good formatting with minor improvements possible. |
| 5-6 | Readable but not optimized for the platform. |
| 3-4 | Wall of text or poor structure. |
| 1-2 | Unreadable on target platform. |

### 7. Platform Fit
Does this content match the platform's algorithm and user behavior?

| Score | Criteria |
|-------|----------|
| 9-10 | Perfectly tailored — length, format, tone all match platform norms. |
| 7-8 | Good fit with minor adjustments needed. |
| 5-6 | Generic content posted to the platform without optimization. |
| 3-4 | Wrong format or tone for the platform. |
| 1-2 | Would actively hurt performance on this platform. |

## Instructions

When given content to score, respond with:

```
## Content QA Report

**Platform**: [detected or specified]
**Content Type**: [post / email / article / script / ad]
**Word Count**: [count]

### Scores

| Dimension | Score | Note |
|-----------|-------|------|
| Hook (2x) | X/10 | [one-line reason] |
| Value Density | X/10 | [one-line reason] |
| Brand Alignment | X/10 | [one-line reason] |
| Engagement Potential | X/10 | [one-line reason] |
| CTA Clarity | X/10 | [one-line reason] |
| Visual/Format | X/10 | [one-line reason] |
| Platform Fit | X/10 | [one-line reason] |

**Weighted Score**: XX/80 (Hook counts 2x)
**Verdict**: [PASS / NEEDS WORK / KILL]

### Top Fix (if not PASS)
[The single highest-leverage change that would improve the score the most]

### Rewrite Suggestion (if NEEDS WORK)
[Rewritten hook or weakest section, demonstrating the improvement]
```

## Verdict Thresholds

- **PASS** (64-80): Publish. This will perform.
- **NEEDS WORK** (40-63): Fix the top issue and re-score. Do not publish as-is.
- **KILL** (0-39): Start over. The core concept or execution is fundamentally weak.

## Example

### Input
> Platform: LinkedIn
> "5 things I learned about sales this year. 1. Follow up matters. 2. Listen more than you talk. 3. Always add value. 4. Be authentic. 5. Never give up. What did you learn? Drop it in the comments!"

### Output

| Dimension | Score | Note |
|-----------|-------|------|
| Hook (2x) | 3/10 | "5 things I learned" is the most overused LinkedIn hook. Zero curiosity. |
| Value Density | 2/10 | All 5 points are cliches with no specificity or stories. |
| Brand Alignment | 4/10 | Too generic to be on-brand for anyone. |
| Engagement Potential | 3/10 | "Drop it in the comments" is lazy engagement bait. |
| CTA Clarity | 5/10 | CTA exists but has no value exchange. |
| Visual/Format | 6/10 | Numbered list is scannable. Line breaks are good. |
| Platform Fit | 5/10 | Right format but algorithm penalizes low-engagement bait posts. |

**Weighted Score**: 31/80
**Verdict**: KILL

**Top Fix**: Replace every generic point with a specific story. "Follow up matters" becomes "I closed a $47K deal because I sent a 9th follow-up that said 'I'm going to stop reaching out — but before I do, here's what you're leaving on the table.'"

---

*Built by [KOINO Capital](https://koino.capital) — Agentic growth systems that run while you sleep.*
*Want this running autonomously 24/7? [Deploy with KOINO](https://koino.capital/deploy)*
