---
name: messaging-orchestrator
description: An orchestration engine to build out a customized Messaging House tuned to your organization through a guided, progressive workflow.
---

# Messaging House Orchestrator

An orchestration engine to build out a customized Messaging House tuned to your organization through a guided, progressive workflow.

## Component Build Sequence

| # | Component | Skill | Purpose |
|---|-----------|-------|---------|
| 1 | Profile | `/messaging-profile` | Core facts (market, type, scale) |
| 2 | Purpose | `/messaging-purpose` | Vision and mission |
| 3 | Portfolio | `/messaging-portfolio` | Products, capabilities, use cases |
| 4 | Proposition | `/messaging-proposition` | Differentiated value |
| 5 | Position | `/messaging-position` | Market landscape and positioning |
| 6 | Pitch | `/messaging-pitch` | Strategic narrative |
| 7 | People | `/messaging-people` | ICP, personas, segments |
| 8 | Proof | `/messaging-proof` | Case studies and social proof |
| 9 | Preferences | `/messaging-preferences` | Voice, tone, style guide |

## Execution Workflow

### Step 0: Check Writing Profile

Read `CLAUDE.md` to check if the writing profile is configured.

**If placeholders exist** (`{role}`, `{company}`, `{stage}`, `{type}`, `{market}`):

```
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
WRITING PROFILE SETUP
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Your writing profile shapes how messaging is generated.
Let's configure it before building your Messaging House.
```

Use `AskUserQuestion` with these questions:

1. **Company name?** (text input)
2. **What role should Claude write as?**
   - Product Marketing Manager
   - Founder / CEO
   - Head of Marketing
   - Content Strategist
   - Other
3. **Company stage?**
   - Emerging (pre-product-market fit)
   - Growing (scaling)
   - Established (market leader)
4. **Company type?**
   - B2B SaaS
   - B2B Services
   - B2C
   - Marketplace / Platform
   - Other
5. **Primary market category?** (text input - e.g., "cybersecurity", "developer tools", "HR tech")

After collecting answers, update the Writing Profile section in `CLAUDE.md`:

```markdown
You are a {role} at {company}. {company} is a(n) {stage} {type} company in the {market} space.
```

**If already configured:** Skip to Step 1.

### Step 1: Check Status

Read `/messaging/*.md` files to determine completion:
- Contains `[Instructions:` → Template/Incomplete
- Has actual content → Complete
- Missing file → Missing

### Step 2: Check Local Research

Scan `/research/` directory:
- List all files present
- Summarize what content is available
- Note what skills can benefit

### Step 3: Display Dashboard

```
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
MESSAGING HOUSE STATUS
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Writing as: {role} at {company} ({stage} {type} in {market})

Progress: [X/9 components complete]

| # | Component   | Status     | Skill                  |
|---|-------------|------------|------------------------|
| 1 | Profile     | ✓ Complete | /messaging-profile     |
| 2 | Purpose     | ✓ Complete | /messaging-purpose     |
| 3 | Portfolio   | ○ Pending  | /messaging-portfolio   |
| 4 | Proposition | ○ Pending  | /messaging-proposition |
| 5 | Position    | ○ Pending  | /messaging-position    |
| 6 | Pitch       | ○ Pending  | /messaging-pitch       |
| 7 | People      | ○ Pending  | /messaging-people      |
| 8 | Proof       | ○ Pending  | /messaging-proof       |
| 9 | Preferences | ○ Pending  | /messaging-preferences |

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

LOCAL RESEARCH (/research/)

[IF files exist:]
Found {N} files:
- {filename}: {brief summary of content type}
- {filename}: {brief summary}

Skills will prioritize this content before searching online.

[IF empty:]
No local research files found.

TIP: Add existing messaging documents to /research/ to reduce web searches:
- About pages, press releases → helps Profile
- Existing messaging, positioning → helps Proposition, Position
- Case studies, testimonials → helps People, Proof
- Brand guidelines → helps Preferences

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

### Step 4: Context Summary

For completed components, extract key context:

```
CONTEXT SUMMARY

Profile: [company] - [type] in [market]
Purpose: Vision: [summary] | Mission: [summary]
Portfolio: [structure] - [N] products, [N] solutions
[etc.]
```

### Step 5: Recommend Next Step

```
RECOMMENDED NEXT

→ Build [Component] using /messaging-[component]

Why: [What this adds and dependencies]
Context available: [What prior context loads]
What to expect: [Research → Present → Confirm flow]
```

### Step 6: Quick Actions

```
What would you like to do?

1. Build recommended component
2. Build different component
3. View context from completed component
4. Add content to /research/ first
5. Update writing profile
```

## Completion Detection

**Complete:** File exists, no `[Instructions:` patterns, has content
**Pending:** File has `[Instructions:` blocks or template only
**In Progress:** Some sections filled, some with instructions
**Missing:** File doesn't exist

## Context Extraction

| Component | Extract |
|-----------|---------|
| Profile | company, type, market, audience, scale |
| Purpose | vision (1 line), mission (1 line) |
| Portfolio | structure, product count, solution count |
| Proposition | value prop one-liners, differentiators |
| Position | landscape summary, positioning core, competitors |
| Pitch | narrative summary, elevator pitch |
| People | ICP summary, persona names, segments |
| Proof | key metrics, customers, analyst recognition |
| Preferences | depth level, tone, tropes to avoid |

## Rules

- Check actual file contents - do not make assumptions
- Route to component skills, don't generate content directly
- Honest completion assessment

## Guidelines

- Keep summaries brief and scannable
- Highlight dependencies for out-of-sequence builds
- Guide users to add local research when beneficial
- Make it easy to resume where they left off
