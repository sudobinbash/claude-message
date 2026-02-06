---
name: messaging-people
description: Build the People component of your Messaging House - the ICP, personas, segments, and customer journey that define who you serve.
---

# Messaging People Builder

Build the **People** - your target audience and how to speak to them.

**Blocks**: ICP | Customer Journey | Personas | Segments

**Dependencies**: Profile, Portfolio, Proposition, Position → audience, products, value props

## Workflow

1. **LOAD CONTEXT**
   Read prior components → Extract: audience, verticals, products, value props
   Scan `/research/` → Look for customer/persona content

2. **RESEARCH GAPS**
   WebSearch (if needed): case studies, testimonials, buyer personas

3. **SYNTHESIZE ICP & PERSONAS**
   Draft ICP from Profile + case study patterns
   Draft personas from testimonials + industry patterns

4. **PRESENT FINDINGS**
   Show customer patterns and draft

5. **CONFIRM & REFINE**
   User validates (4 questions)

6. **GENERATE**
   Create blocks → Write to `/messaging/people.md` → Validate

## Research

### Priority Order
1. Scan `/research/` for customer/persona content
2. Read prior components
3. WebSearch only for gaps

### Queries (if needed)
| Query | Purpose |
|-------|---------|
| `"{company} case studies"` | Real customer profiles |
| `"{company} testimonials"` | Persona language/titles |
| `"{market category} buyer persona"` | Industry patterns |

### Extract
- Customer profiles: industry, size, region
- Titles/roles: from testimonials, case studies
- Pain points: challenges mentioned
- Outcomes: results achieved

## Generation Approach

### Key Mental Model
For each persona, ask: **What are they "on the hook for" and what are they "on the hunt for"?**

Frame value messaging as: **Current State → Desired State → How to Get There → Why Only Us**

### ICP
Define **eligibility**, not aspiration. Who this is for AND who this is NOT for.

**How to generate:**
- Disqualifying conditions: Be specific and honest
- Characteristics: Structural traits (complexity, scale, regulations)
- Behaviors: Observable signals (budget, risk, operational strain)
- Environment: People, process, technology considerations
- Maturity: Where good-fit customers typically are

**Quality filter:** Would a salesperson use this to qualify leads?

### Customer Journey
How messaging evolves as awareness changes.

**How to generate:**
- Awareness: Make them care about the problem
- Consideration: Show you understand and have an answer
- Evaluation: Prove you can deliver
- Decision: Remove remaining objections

For each stage: Goal, Walk Away Feeling, Key Messages, Best Proof

### Personas & Segments
Reference profiles, don't reinvent in this file.

**Location:** `/messaging/personas/` and `/messaging/segments/`

## Present Findings

```
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
RESEARCH FINDINGS: PEOPLE
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

CONTEXT (from Profile):
- Target Audience: {from Profile}
- Verticals: {from Profile}

CUSTOMER PATTERNS (from case studies):
Industries: [list]
Company sizes: [pattern]

PERSONAS FOUND:
- [Title 1] - appeared in [X] case studies
- [Title 2] - common buyer role

DRAFT ICP:
- Company type: [description]
- Size: [range]
- Characteristics: [traits]
- Behaviors: [signals]
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

## Confirm & Refine

4 questions maximum:

1. **Is this ICP accurate?**
   - [ ] Yes / Adjust: [describe] / Add disqualifying conditions

2. **Are these the right personas?**
   - [ ] Yes / Missing: [add] / Remove: [which] / Adjust titles

3. **Primary pain point for each persona?**
   [Persona 1]: [pain]
   [Persona 2]: [pain]

4. **Need segment-specific messaging?**
   - [ ] No, ICP sufficient
   - [ ] By industry: [verticals]
   - [ ] By size: [enterprise vs mid-market]

## Output Format

Write to `/messaging/people.md`:

```markdown
# Messaging House - People

The People defines our target audience with relevant characteristics and behaviors to align messaging to.

Use this section to ensure precision and resonance. Messaging should only target audiences that meet ICP criteria, then be tailored by segment and persona when applicable.

## Messaging Blocks

### Ideal Customer Profile (ICP)

#### Disqualifying Conditions
[Who this is NOT for - be specific]

#### Characteristics
[Structural traits of good fit - complexity, scale, regulations, operating model]

#### Behaviors
[Observable signals of pain, urgency, or readiness]

#### Environment
[People, process, technology considerations]

#### Maturity
[Where good-fit customers typically are in their journey]

### Customer Journey

#### Awareness
**Goal:** Make them care about the problem
**Walk Away Feeling:** "Wow. Yes, that's a real pain point I'd like to solve."
**Key Messages:** [High-level problem framing, industry shifts]
**Best Proof:** [Trends, insights, third-party perspectives]

#### Consideration
[Same structure]

#### Evaluation
[Same structure]

#### Decision
[Same structure]

### Persona Profiles

When specific personas are related to your task, extract from `/messaging/personas/`.

| Persona | File |
|---------|------|
| [Persona A] | persona-a.md |

### Segment Profiles

When specific segments are related to your task, extract from `/messaging/segments/`.

| Segment | File |
|---------|------|
| [Segment A] | segment-a.md |

## Rules

- ICP defines eligibility — if ICP conditions are not met, assume no fit
- Validate ICP fit before refining to specific segments and personas
- Do not invent personas or segments beyond those defined

## Guidelines

- Use ICP signals to determine whether urgency is inferred or needs to be established
- Personas influence tone, direction, and value emphasis — not positioning
- Segments adapt context and emphasis, not value propositions
```

## Validation

- [ ] Checked `/research/` before searching
- [ ] ICP disqualifying conditions are specific (not generic)
- [ ] Personas based on real roles from case studies
- [ ] Pain points grounded in market context
- [ ] Journey stages have consistent structure
