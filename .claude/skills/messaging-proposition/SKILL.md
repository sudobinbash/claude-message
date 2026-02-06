---
name: messaging-proposition
description: Build the Proposition component of your Messaging House - the unique value propositions that anchor all value-led messaging.
---

# Messaging Proposition Builder

Build the **Proposition** - unique value you deliver and why it matters.

**Blocks**: Unique Value Propositions (3-5 pillars)

**Dependencies**: Profile, Purpose, Portfolio → audience, products, solutions, vision

## Workflow

1. **LOAD CONTEXT**
   Read Profile, Purpose, Portfolio → Extract: audience, products, solutions, vision
   Scan `/research/` → Look for value prop, differentiation content

2. **SYNTHESIZE**
   From Portfolio: What outcomes do solutions deliver?
   From Purpose: What vision guides the value?

3. **RESEARCH GAPS**
   WebSearch (if needed): company benefits, competitor value props

4. **PRESENT DRAFT**
   Show synthesized value props with reasoning

5. **CONFIRM & REFINE**
   User validates, adjusts, provides supporting messages (2-3 questions)

6. **GENERATE**
   Create blocks → Write to `/messaging/proposition.md` → Validate

## Synthesis Approach

Value propositions should be **derived**, not invented:

1. **Start with Portfolio solutions** - Each solution delivers a specific outcome. What is it?
2. **Test against competitors** - Could they credibly make the same claim?
3. **Connect to Purpose** - Does this value align with the vision?
4. **Focus on outcomes** - Measurable results, not features or capabilities

**Quality filters:**
- Each proposition stands alone as a key message
- Tied to funded customer problems (real pain, not hypothetical)
- Specific enough that competitors can't claim it
- Outcome-focused, not feature-focused

## Present Draft

```
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
SYNTHESIZED VALUE PROPOSITIONS
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

CONTEXT USED:
- Vision: {from Purpose}
- Solutions: {from Portfolio}

VALUE PROP 1: [Name]
One-liner: [Draft]
Why it matters: [Buyer impact]
Why we're different: [Uniqueness]
Portfolio mapping: [Products/solutions]

VALUE PROP 2: [Name]
[Same structure]

REASONING:
- VP1 derived from [Portfolio solution] + [Purpose vision]
- VP2 addresses [outcome] differentiating from [alternative]
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

## Confirm & Refine

2-3 questions maximum:

1. **Do these capture your key outcomes?**
   - [ ] Yes / Adjust: [describe] / Missing: [add] / Remove: [which]

2. **Are one-liners clear and differentiated?**
   - [ ] Yes / Adjust wording / Too similar to competitors

3. **Supporting messages for each?**
   Provide 3 bullets per value prop

## Block Structure

### Unique Value Propositions

Each value proposition should include:

| Element | What it is | How to generate |
|---------|-----------|-----------------|
| **One-Liner** | The differentiated outcome in 1 sentence | Derive from Portfolio solution outcome |
| **Supporting Messages** | 3 bullets expanding on outcome | Add context, specificity, proof direction |
| **Why It Matters** | Buyer impact or risk addressed | Connect to funded customer problems |
| **Why We're Different** | What makes this uniquely yours | Test: could a competitor say this? |
| **Portfolio Mapping** | Products/solutions this applies to | Direct link to Portfolio |

**Target:** 3-5 propositions total (fewer is stronger)

## Output Format

Write to `/messaging/proposition.md`:

```markdown
# Messaging House - Proposition

Our Proposition defines the unique value we deliver to customers and why it matters.

Use this section as the primary source of value messaging that should be reflected across all messaging and content assets.

## Messaging Blocks

### Unique Value Propositions

#### [Value Prop 1 Name]

**One-Liner:** [Differentiated outcome]

**Supporting Messages:**
- [Message 1]
- [Message 2]
- [Message 3]

**Why It Matters:** [Buyer impact]

**Why We're Different:** [Uniqueness]

**Portfolio Mapping:** [Products: X. Solutions: A.]

---

#### [Value Prop 2 Name]

[Same structure]

---

## Rules

- Value propositions are durable messaging pillars
- Each proposition stands on its own as a key message

## Guidelines

- Treat value propositions as durable messaging pillars
- Anchor benefits and outcomes to the closest matching proposition
- Introduce product capabilities to support a value proposition
```

## Validation

- [ ] Checked `/research/` and prior components
- [ ] Value props derived from Portfolio solutions
- [ ] Each one-liner is outcome-focused (not feature-focused)
- [ ] Each is specific enough competitors can't claim it
- [ ] 3-5 total (not too few, not too many)
