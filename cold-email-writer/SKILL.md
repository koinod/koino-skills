# Cold Email Writer

> Write personalized cold emails that get replies. 3-5 sentences. One CTA. No fluff.

## Description

Cold Email Writer generates hyper-personalized outbound emails given a company name, industry, and pain point. Every email follows the P.A.S. + 1 CTA formula that top SDRs use to hit 15%+ reply rates. The output is ready to send — no editing required.

The difference between a 2% reply rate and a 15% reply rate is personalization and brevity. This skill handles both.

## Activation

This skill activates when:
- The user wants to write a cold email or outbound message
- The user provides a prospect's company and wants to reach out
- The user asks for email copy, outreach templates, or cold outreach help
- The user mentions prospecting, outbound sales, or email campaigns

**Trigger phrases**: "write a cold email", "outreach email", "email this prospect", "cold outbound", "prospecting email", "reach out to", "email copy"

## The P.A.S. + 1 CTA Formula

### P — Personalized Opening (1 sentence)
Reference something specific about THEM. Not "I hope this finds you well." Something that proves you spent 30 seconds looking at their business.

Sources for personalization:
- Recent LinkedIn post or company announcement
- Their website copy or a specific product/service they offer
- Industry trend affecting their segment
- A mutual connection or shared community
- Their job title + likely daily pain

### A — Agitate the Pain (1-2 sentences)
Name the specific problem they face. Make it visceral. Use their language, not yours.

### S — Solution Tease (1 sentence)
Hint at how you solve it. Do NOT explain your full solution. Create curiosity.

### 1 CTA — One Clear Ask (1 sentence)
One question. Low friction. Easy to say yes to.

**Good CTAs**: "Worth a 12-minute call this week?" / "Can I send a 2-minute video showing how?" / "Want me to run a free audit?"

**Bad CTAs**: "Let me know if you're interested" / "Would love to connect" / "Check out our website"

## Instructions

When given prospect details, generate:

```
**Subject**: [5-8 words, curiosity-driven, no spam triggers]

[Personalized opening — reference something specific about them]

[Agitate — name their pain, make it real]

[Solution tease — hint at the fix without explaining everything]

[CTA — one question, low friction]

[First name only sign-off]

---

**Why this works**: [1-2 sentences on the psychology]
**Follow-up (send 3 days later if no reply)**: [2-sentence bump email]
```

## Rules

1. **3-5 sentences total.** Not 3-5 paragraphs. Sentences.
2. **No "I" in the first sentence.** Start with THEM.
3. **No buzzwords**: "synergy", "leverage", "revolutionary", "game-changing" — all banned.
4. **No attachments or links** in cold email #1. They trigger spam filters and reduce trust.
5. **Subject line**: No caps lock, no emojis, no "RE:" tricks. Write it like a colleague would.
6. **Reading level**: 5th grade. Short sentences. Common words.
7. **Mobile-first**: 80% of cold emails are read on phones. If it looks like a wall of text on mobile, rewrite.

## Example

### Input
> Company: Apex HVAC Services. Industry: Home services / HVAC. Pain point: Losing leads because they take 4+ hours to respond to website inquiries. Owner: Dave. 12 technicians, $1.2M revenue.

### Output

**Subject**: your website leads on Saturday

Dave — noticed Apex is running Google Ads to your quote request form. Solid setup.

Here's the thing: 78% of home service leads go with whoever responds first. If your team is taking 4+ hours to reply (especially on weekends), you're paying for leads your competitors are closing.

We built a system that responds to every inquiry in under 90 seconds — 24/7, including nights and weekends — with a personalized message, not a generic autoresponder.

Worth a 12-minute call this week to see if it fits?

Dave's-name-here

---

**Why this works**: Opens with proof of research (Google Ads). Uses a real stat (78% first-responder wins) to make the pain concrete. Solution tease creates curiosity without over-explaining. CTA is specific (12 minutes) and low-friction.

**Follow-up (send 3 days later if no reply)**:
"Dave — quick bump on this. Ran the numbers: at $1.2M revenue with 12 techs, even recovering 3 lost leads/month would be worth $15-20K/year. Happy to show you the math in 10 minutes."

## Variations

### The Mutual Connection Angle
When you share a connection:
> "[Connection name] mentioned you're dealing with [pain]. We just helped [similar company] solve the same thing — [specific result]. Worth comparing notes?"

### The Insight Lead
When you have industry data:
> "Pulled data on [their industry] this week — companies your size are losing an average of $X/month to [problem]. Most don't realize it until [consequence]. Quick question: [CTA]"

### The Breakup Email (Final follow-up)
> "Dave — I've reached out a couple times. I'll assume the timing isn't right and close your file. If [pain point] becomes a priority, I'm here. Either way, good luck with the spring rush."
> (This gets the highest reply rate of any email in a sequence — 22% average.)

## Batch Mode

Provide a CSV or list of prospects and receive personalized emails for each:

```
| Company | Contact | Industry | Pain Point |
|---------|---------|----------|------------|
| Apex HVAC | Dave | Home services | Slow lead response |
| GreenTree | Mike | Landscaping | Admin overwhelm |
| BluePeak | Sarah | Dental | No-shows |
```

Each email will be uniquely personalized — not a mail merge with swapped names.

---

*Built by [KOINO Capital](https://koino.capital) — Agentic growth systems that run while you sleep.*
*Want this running autonomously 24/7? [Deploy with KOINO](https://koino.capital/deploy)*
