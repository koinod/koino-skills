---
name: workflow-auditor
description: Audit your business workflows and find automation opportunities
version: 1.0.0
author: KOINO Capital
license: MIT
tags: [automation, workflows, efficiency, audit, operations, roi]
---

# Workflow Auditor

Find the hidden time and money leaks in your business. This skill walks you through a structured audit of your workflows and delivers a ranked list of automation opportunities with estimated ROI.

## How It Works

This is an **interactive audit**. Answer the questions honestly -- the output is only as good as the input. The full audit takes 10-15 minutes and can save you hundreds of hours per year.

---

## Phase 1: Business Context (2 minutes)

Answer these to calibrate the audit:

1. **What does your business do?** (1-2 sentences)
2. **How many people are on your team?** (include yourself)
3. **What's your approximate annual revenue?** (or range: <$100K, $100K-$500K, $500K-$1M, $1M-$5M, $5M+)
4. **What tools do you currently use?** (CRM, email, spreadsheets, project management, accounting, etc.)
5. **Have you automated anything before?** (Yes/No, and what?)

---

## Phase 2: Workflow Discovery (5-8 minutes)

For each of these 8 business areas, describe what you currently do. Skip any that don't apply.

### Area 1: Lead Generation & Sales
- How do leads find you? (inbound, outbound, referrals, ads)
- What happens when a new lead comes in? Walk through each step.
- How do you track leads? (CRM, spreadsheet, memory, sticky notes)
- How long from first contact to closed deal (average)?
- What's your follow-up process? (manual emails, sequences, nothing)

### Area 2: Client Onboarding
- What happens after someone says "yes"?
- How many manual steps between signed contract and work starting?
- Do you send welcome emails, intake forms, or kickoff docs?
- How long does onboarding take?

### Area 3: Service Delivery / Fulfillment
- What's your core deliverable and how is it produced?
- Which steps require human judgment vs. which are repetitive?
- How do you track project status?
- How do you communicate progress to clients?

### Area 4: Communication & Meetings
- How many emails do you send/receive per day?
- How many meetings per week? How long are they?
- Do you take meeting notes? How?
- How do you share information across the team?

### Area 5: Content & Marketing
- Do you create content? (social, blog, email, video)
- How long does one piece of content take to create?
- How do you repurpose content across platforms?
- What's your posting frequency?

### Area 6: Finance & Admin
- How do you create and send invoices?
- How do you track expenses?
- How much time per week on bookkeeping and admin?
- Do you manually enter data between systems?

### Area 7: Hiring & Team Management
- How do you find and evaluate candidates?
- How do you onboard new team members?
- How do you assign and track tasks?
- How do you handle time tracking or performance reviews?

### Area 8: Customer Support & Retention
- How do customers reach you for help?
- What's your average response time?
- Do you have documented processes or SOPs?
- How do you collect feedback or testimonials?

---

## Phase 3: Analysis & Scoring

After collecting responses, analyze each workflow against the **Automation Opportunity Matrix**:

### Scoring Criteria

For each identified workflow, score on 4 dimensions:

| Dimension | Question | Scale |
|-----------|----------|-------|
| **Frequency** | How often is this done? | 1 (monthly) to 10 (multiple times daily) |
| **Time Cost** | How long does it take each time? | 1 (<5 min) to 10 (2+ hours) |
| **Error Rate** | How often do mistakes happen? | 1 (rarely) to 10 (frequently) |
| **Automation Feasibility** | Can current tools automate this? | 1 (needs custom AI) to 10 (off-the-shelf solution exists) |

**Automation Priority Score** = (Frequency x 2) + (Time Cost x 2) + (Error Rate x 1.5) + (Feasibility x 1.5)

- **Max score: 70**
- **50+**: Automate immediately -- you're burning money
- **35-49**: Strong candidate -- plan for next quarter
- **20-34**: Nice to have -- automate when you've handled the big ones
- **Under 20**: Leave it manual for now

---

## Phase 4: Output

### 1. Executive Summary

```
BUSINESS: [Name]
TEAM SIZE: [X]
WORKFLOWS AUDITED: [X]
AUTOMATION OPPORTUNITIES FOUND: [X]
ESTIMATED ANNUAL TIME SAVINGS: [X hours]
ESTIMATED ANNUAL COST SAVINGS: $[X] (at $[hourly rate]/hr)
```

### 2. Ranked Opportunity List

For each opportunity, ranked by priority score:

```
#[Rank]: [Workflow Name]
Priority Score: [X]/70
Category: [AUTOMATE NOW / PLAN FOR Q2 / NICE TO HAVE / SKIP]

Current State:
[2-3 sentences describing what they do now and why it's inefficient]

Recommended Automation:
[2-3 sentences describing the specific automation approach]

Tools/Approach:
- [Tool 1]: [What it handles]
- [Tool 2]: [What it handles]
- [Alternative if budget is $0]: [Free tool or approach]

Estimated Time Savings: [X hours/week]
Estimated Annual Savings: $[X]
Implementation Difficulty: [EASY / MEDIUM / HARD]
Implementation Time: [X hours/days]

Quick Win: [1 sentence -- something they can do TODAY in under 30 minutes
to start capturing value]
```

### 3. Implementation Roadmap

Group opportunities into phases:

**Phase 1 -- This Week (Quick Wins):**
- Changes that take under 2 hours and save immediate time
- Usually: email templates, form automation, simple integrations

**Phase 2 -- This Month (Foundation):**
- Core workflow automations that require some setup
- Usually: CRM workflows, invoicing automation, content scheduling

**Phase 3 -- This Quarter (Scale):**
- Larger automations that compound the Phase 1-2 gains
- Usually: AI-assisted processes, custom integrations, reporting dashboards

**Phase 4 -- Next Quarter (Advanced):**
- Complex automations requiring custom development or AI
- Usually: predictive analytics, autonomous agents, custom platforms

### 4. Tool Recommendations

For each recommended tool, provide:

| Tool | What It Solves | Cost | Free Alternative |
|------|---------------|------|-----------------|
| [Tool] | [Use case] | [$/mo] | [Free option] |

**Always include a $0 path.** Not everyone has budget for tools, and scrappy solutions that work beat expensive tools that don't get implemented.

### 5. Hidden Costs Identified

Things the business owner may not realize they're spending money on:

- **Context switching**: Jumping between X tools costs ~Y hours/week
- **Manual data entry**: Entering the same info in X places wastes ~Y hours/week
- **No templates**: Rewriting the same emails/docs from scratch wastes ~Y hours/week
- **Meeting overhead**: X hours of meetings that could be async updates
- **Error correction**: Fixing mistakes from manual processes costs ~Y hours/week

---

## Common Automation Patterns

### The "Copy-Paste" Pattern
**Symptom**: Same information entered in multiple systems
**Fix**: Integration/API connection or single source of truth
**Tools**: Zapier, Make, n8n (free), native integrations

### The "Reminder" Pattern
**Symptom**: Things fall through cracks without manual tracking
**Fix**: Automated triggers and notifications
**Tools**: CRM workflows, calendar automations, task management rules

### The "Template" Pattern
**Symptom**: Rewriting similar documents/emails from scratch
**Fix**: Templates with variable fields, auto-populated from your data
**Tools**: Email sequences, document generators, form-to-doc tools

### The "Report" Pattern
**Symptom**: Hours spent pulling data and building reports
**Fix**: Auto-generated dashboards that update in real-time
**Tools**: Google Sheets + scripts, Notion databases, BI tools

### The "First Response" Pattern
**Symptom**: Leads/customers wait hours for initial response
**Fix**: Auto-responders, chatbots, or AI-assisted triage
**Tools**: Email autoresponders, chatbot builders, AI assistants

---

## After the Audit

Your ranked opportunity list is the starting point. Here's how to act on it:

1. **Pick the top-scored opportunity.** Just one. Don't try to automate everything at once.
2. **Implement the Quick Win today.** Each opportunity has one -- do it now.
3. **Block 2 hours this week** to set up the Phase 1 automation for your #1 opportunity.
4. **Measure the before/after.** Track time spent before and after automation. You need proof it works.
5. **Move to #2 once #1 is stable.** Rushing automation creates more problems than it solves.

Want help implementing? We build these systems for businesses every day.

**Get the full implementation at [koino.capital/contact](https://koino.capital/contact)**

---

*Powered by [KOINO Capital](https://koino.capital) -- we find the leaks in your business and plug them with AI.*
