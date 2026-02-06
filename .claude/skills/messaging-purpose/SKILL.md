---
name: messaging-purpose
description: Build the Purpose component of your Messaging House - the company vision and mission that anchor your positioning and messaging direction.
---

# Messaging Purpose Builder

Build the **Purpose** - why your company exists in the market.

**Blocks**: Company Vision | Mission Statement

**Dependencies**: Profile → company_name, market_category, target_audience

## Workflow

1. **LOAD CONTEXT**
   Read Profile → Extract: company_name, market_category, target_audience
   Scan `/research/` → Look for vision/mission content

2. **RESEARCH GAPS**
   WebSearch (if needed): about page, careers, mission, vision, values

3. **PRESENT FINDINGS**
   Show existing statements or draft alternatives

4. **CONFIRM & REFINE**
   User validates vision and mission (2-3 questions)

5. **GENERATE**
   Create blocks → Write to `/messaging/purpose.md` → Validate

## Research

### Priority Order
1. Scan `/research/` for vision/mission content
2. Read `/messaging/profile.md` for company context
3. WebSearch only for gaps

### Queries (if needed)
| Query | Purpose |
|-------|---------|
| `"{company} about us"` | Vision/mission on about page |
| `"{company} mission"` | Direct mission search |
| `"{company} careers culture"` | Mission often on careers page |

## Generation Approach

### Company Vision
The North Star - a future world the company is driving towards.

**How to generate:**
- Focus on external market forces, not internal company goals
- Be directional and opinionated - take a stance
- Avoid generic phrases that could be anyone

**Good:** "Security that keeps pace with innovation, not the other way around"
**Bad:** "To be the leading provider of..." (internal goal, not vision)

**Quality filter:** Could a competitor claim this? If yes, sharpen it.

**Format:** 1-2 sentences describing a changed future state

### Mission Statement
The daily drumbeat - what the company does every day to realize the vision.

**How to generate:**
- Emphasize verbs and ongoing behavior
- Align to the vision with the how
- Avoid abstract language

**Good:** "We automate security workflows so teams can focus on threats that matter"
**Bad:** "Our mission is customer success" (doesn't describe what you do)

**Format:** 1-2 sentences describing a continuous discipline

## Output Format

Write to `/messaging/purpose.md`:

```markdown
# Messaging House - Purpose

Our Purpose is why our company exists in the market.

Use this section as root context to shape our POV and our ambition across our messaging. This section should influence framing and direction, not be quoted verbatim unless explicitly requested.

## Messaging Blocks

### Company Vision

[1-2 sentences: future world you're driving towards. External, directional, opinionated.]

### Mission Statement

[1-2 sentences: what you do every day. Action verbs, ongoing behavior, aligns to vision.]

## Usage Guidelines

- Use Company Vision to shape aspirational framing, narrative arc, and industry-level language
- Use Mission Statement to ground claims in practicality and credibility
- Do not restate Purpose verbatim unless explicitly instructed
- When in tension with other elements, Purpose sets direction, not details
```

## Validation

- [ ] Checked `/research/` and Profile before searching
- [ ] Reused existing statements where available
- [ ] Vision: 1-2 sentences, external focus, takes a stance
- [ ] Mission: 1-2 sentences, action-oriented, connects to vision
- [ ] Both are specific enough that competitors couldn't claim them
