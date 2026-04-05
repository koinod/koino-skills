# Cold Outreach

> Generate a personalized 5-touch email sequence + 3 LinkedIn DM variants for any prospect.

---
name: cold-outreach
version: 1.0.0
description: Generate personalized cold outreach sequences using proven sales frameworks
author: KOINO Capital
tags: [sales, outreach, email, linkedin, prospecting]
---

## Description

Cold Outreach generates a full multi-channel outreach sequence — 5 emails + 3 LinkedIn DMs — personalized to a specific prospect. Every message uses battle-tested copywriting frameworks (PAS, BAB, AIDA) that top sellers use to book meetings. No generic templates. No "I hope this finds you well."

The difference between a full pipeline and an empty calendar is 8 well-written messages.

## Activation

This skill activates when:
- The user wants to create a cold outreach sequence or campaign
- The user provides a prospect and wants email + LinkedIn messages
- The user asks for a drip sequence, follow-up emails, or outbound campaign
- The user mentions "cold outreach", "email sequence", "follow-up sequence", or "DM script"

**Trigger phrases**: "cold outreach", "outreach sequence", "email sequence for", "follow-up emails", "LinkedIn DMs", "drip campaign", "prospect sequence", "how to reach out to"

## Input

The user provides some or all of:
- **Prospect name** — who you're reaching out to
- **Company** — where they work
- **Title/role** — their position
- **Industry** — their vertical
- **Pain point** — what problem you solve for them
- **Your offer** — what you're selling or proposing
- **Context** (optional) — mutual connection, recent event, anything specific

If the user provides minimal info, ask for at least: company, industry, and pain point. Infer the rest.

## Instructions

### Step 1: Build the Prospect Profile

From the input, establish:
- **Their likely daily reality** — what does their day look like?
- **Their top 3 pains** — what keeps them up at night?
- **Their buying triggers** — what would make them act NOW vs. later?
- **Their objections** — why would they say no or ignore you?
- **Their language** — how do they talk about their problems? (industry jargon, casual, formal)

### Step 2: Generate the 5-Email Sequence

Each email uses a different framework and escalation level:

---

```markdown
## Email Sequence

### Email 1: The Opener (Day 1)
**Framework**: Problem-Agitate-Solve (PAS)
**Goal**: Earn a reply. Not a meeting. A reply.

**Subject**: [5-8 words, lowercase, curiosity-driven]

[Personalized opening — reference something specific about THEM (1 sentence)]

[Agitate — name the pain, make it visceral (1-2 sentences)]

[Solution tease — hint at how you solve it without explaining everything (1 sentence)]

[CTA — one low-friction question (1 sentence)]

[First name sign-off]

---

### Email 2: The Value Drop (Day 3)
**Framework**: Before-After-Bridge (BAB)
**Goal**: Provide value. Build credibility. No ask yet.

**Subject**: [Reference to Email 1 or new angle]

[Before — paint their current reality (1-2 sentences)]

[After — paint what life looks like with the problem solved (1-2 sentences)]

[Bridge — "Here's how [similar company] got there" + specific result (1-2 sentences)]

[Soft CTA — "Want me to show you exactly how?" or share a resource]

---

### Email 3: The Social Proof (Day 7)
**Framework**: Case Study Drop
**Goal**: Overcome the "why should I trust you" objection.

**Subject**: [Reference a result, not your company]

[1-sentence re-engagement — "Quick follow-up on [topic]"]

[Mini case study — Company X had [same problem]. We [did this]. Result: [specific metric]. (2-3 sentences)]

[Bridge to them — "Your situation at [their company] looks similar because [reason]." (1 sentence)]

[CTA — specific and time-bound: "Got 15 minutes Thursday or Friday?"]

---

### Email 4: The Pattern Interrupt (Day 12)
**Framework**: Curiosity + Contrast
**Goal**: Break through inbox blindness. Change the pattern.

**Subject**: [Unexpected angle — question, stat, or contrarian take]

[Pattern interrupt — say something they haven't heard from the other 47 salespeople in their inbox (1-2 sentences)]

[Quick reframe of the problem from a new angle (1-2 sentences)]

[Micro-CTA — even lower friction than before: "Yes or no — worth a conversation?"]

---

### Email 5: The Breakup (Day 18)
**Framework**: Loss Aversion + Dignity
**Goal**: Trigger FOMO or get a definitive no (both are wins).

**Subject**: "closing your file" or "should I stop reaching out?"

[Acknowledge — "I've reached out a few times and haven't heard back. I get it — you're busy." (1 sentence)]

[Quick restate of value — one sentence, the strongest version (1 sentence)]

[Breakup — "I'll close your file and won't reach out again. If [pain point] becomes a priority, here's my calendar link." (1 sentence)]

[Graceful close — wish them well, no guilt trip]

*Note: This email consistently gets the highest reply rate (18-25%) because it triggers loss aversion.*
```

---

### Step 3: Generate 3 LinkedIn DM Variants

```markdown
## LinkedIn DM Variants

### DM 1: The Connection Request Note (300 chars max)
**Approach**: Peer-to-peer, no pitch

[Reference shared industry, mutual connection, or their content (1 sentence)]
[Reason for connecting — NOT to sell (1 sentence)]

*Example tone: "Saw your post on [topic] — sharp take. I work in the same space and wanted to connect."*

---

### DM 2: The Follow-Up DM (after they accept — Day 2)
**Approach**: Give before you ask

[Thank them for connecting (1 sentence)]
[Offer something valuable — insight, resource, or observation about their business (2-3 sentences)]
[No ask. Just value.]

---

### DM 3: The Pivot to Conversation (Day 5-7)
**Approach**: Natural transition from connection to conversation

[Reference something from their recent activity — post, comment, company news (1 sentence)]
[Tie it to the pain point naturally (1 sentence)]
[Soft CTA — "Curious how you're handling [specific challenge]?" or "Happy to share what's working for [similar companies] if useful."]
```

---

### Step 4: Sequence Strategy Notes

```markdown
## Sequence Strategy

**Timing**:
| Touch | Channel | Day | Best Send Time |
|-------|---------|-----|----------------|
| Email 1 | Email | Day 1 | Tue-Thu, 8-9am |
| DM 1 | LinkedIn | Day 1 | Same day as Email 1 |
| Email 2 | Email | Day 3 | 8-9am |
| DM 2 | LinkedIn | Day 4 | After they accept |
| Email 3 | Email | Day 7 | 8-9am |
| DM 3 | LinkedIn | Day 9 | 10am-12pm |
| Email 4 | Email | Day 12 | 7-8am (early = pattern interrupt) |
| Email 5 | Email | Day 18 | 3-4pm Fri (end of week reflection) |

**If they reply at any point**: STOP the sequence. Respond personally. Never send the next automated touch after a reply.

**If no reply after all 8 touches**: Wait 45 days, then restart with a completely new angle. Never repeat the same sequence.

**Objection handling**:
- "Not interested" → "Totally fair. Mind if I ask — is it the timing or the concept?"
- "We already have a solution" → "Good to hear. Out of curiosity, what's working and what's not?"
- "Send me more info" → "Happy to. What specifically would be most useful — [option A] or [option B]?" (qualify, don't just dump a PDF)
- "Too expensive" → "Makes sense to think about cost. When you say expensive — compared to what?"
```

## Rules

1. **Personalization is mandatory.** Every email must reference something specific about the prospect or their company. No "Dear Sir/Madam."
2. **3-5 sentences per email.** These are cold emails, not whitepapers.
3. **One CTA per message.** Never two. Never zero.
4. **No buzzwords.** "Synergy", "leverage", "revolutionary", "game-changing", "cutting-edge" — all banned.
5. **Subject lines are lowercase.** No caps. No emojis. No "RE:" tricks. Write like a colleague, not a marketer.
6. **Each email stands alone.** If they only read Email 3, it should still make sense.
7. **Escalate, don't repeat.** Each touch adds a new angle, new proof point, or new frame. Never say the same thing twice.
8. **Mobile-first.** 80% of emails are read on phones. No walls of text.
9. **No attachments or links in Email 1.** They trigger spam filters.

## Example

### Input
> Prospect: Sarah Chen, VP of Sales at CloudMetrics (Series B SaaS, 200 employees). Industry: Analytics/BI. Pain point: Their SDR team books meetings but 40% no-show. My offer: AI-powered meeting confirmation and prep system.

### Output
*(Full 5-email sequence + 3 LinkedIn DMs following the exact format above, personalized to Sarah, CloudMetrics, and the no-show problem)*

## Batch Mode

Provide a list of prospects to generate unique sequences for each:

```
| Name | Company | Role | Industry | Pain Point |
|------|---------|------|----------|------------|
| Sarah Chen | CloudMetrics | VP Sales | SaaS/Analytics | 40% meeting no-shows |
| Marcus Rivera | GreenBuild | COO | Construction | Project delays from manual scheduling |
| Priya Patel | HealthSync | CMO | HealthTech | Low content output despite 5-person team |
```

Each sequence will be uniquely crafted — not a find-and-replace.

---

*Built by [KOINO Capital](https://koino.capital) | Test your outreach with our cognitive sim: [koino.capital/simulate](https://koino.capital/simulate)*
*Want outreach sequences generated and sent autonomously? [Deploy with KOINO](https://koino.capital/deploy)*
