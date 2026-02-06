---
name: messaging-pitch
description: Build the Pitch component of your Messaging House - the strategic narrative and elevator pitch that explains why change is necessary and why you are uniquely positioned to lead it.
---

# Messaging Pitch Builder

Build the **Pitch** - strategic narrative synthesizing all prior components.

**Blocks**: Strategic Narrative (9-part arc) | Elevator Pitch (30-60 sec)

**Dependencies**: Profile, Purpose, Portfolio, Proposition, Position

## Workflow

1. **LOAD ALL CONTEXT**
   Read all prior components → Extract key elements for narrative synthesis
   Scan `/research/` → Look for pitch/narrative content

2. **RESEARCH GAPS**
   WebSearch (if needed): market challenges, trends, statistics

3. **SYNTHESIZE NARRATIVE**
   Map prior components to 9-part arc

4. **PRESENT DRAFT**
   Show narrative with source attribution

5. **CONFIRM & REFINE**
   User validates flow (2-3 questions)

6. **GENERATE**
   Create blocks → Write to `/messaging/pitch.md` → Validate

## Generation Approach

### Key Principle
**Your narrative is more about your audience than it is about you.** The stronger the inflection, the greater the urgency. Even with structure, write in a conversational tone.

### Narrative Arc

Build the narrative from prior components:

| Element | Source | What to generate |
|---------|--------|------------------|
| **The Scenario** | Position (landscape) | Attention hook - current conditions facing audience |
| **The Inflection** | Position (forces) | Industry forces making this urgent |
| **The Status Quo** | Position (alternatives) | Why existing approaches fail |
| **Our Smart Insight** | Proposition (differentiation) | What you figured out others missed |
| **Our Unique Approach** | Portfolio + Position | What you built and why it's different |
| **Our Proof of Value** | Proof points | Tangible evidence (quotes, mentions) |
| **Reason to Believe** | Purpose (vision) | What audience can advocate for |
| **Undeniable Gain** | Proposition (value props) | Quantitative/qualitative outcomes |
| **Step to Action** | - | Tangible next steps (not a CTA) |

**Flow:** First 3 create urgency (Scenario → Inflection → Status Quo). Next 3 establish credibility (Insight → Approach → Proof). Final 3 inspire action (Believe → Gain → Action).

### Elevator Pitch
30-60 seconds, conversational, assumes no context.

**How to generate:**
- All bangers, no filler - keep it tight
- Hit key beats: problem → insight → approach → gain
- Natural spoken language, not scripted

## Present Draft

```
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
SYNTHESIZED STRATEGIC NARRATIVE
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

SOURCE MAPPING:
- Scenario: Position (landscape)
- Inflection: Position (forces) + Purpose (vision)
- Status Quo: Position (alternatives)
- Smart Insight: Proposition (differentiation)
- Unique Approach: Portfolio + Position
- Proof of Value: Proof points
- Reason to Believe: Purpose (vision)
- Undeniable Gain: Proposition (value props)

THE SCENARIO: [Draft hook]
THE INFLECTION: [Draft urgency]
THE STATUS QUO: [Draft why alternatives fail]
OUR SMART INSIGHT: [Draft what you figured out]
OUR UNIQUE APPROACH: [Draft solution]
OUR PROOF OF VALUE: [Draft credibility]
REASON TO BELIEVE: [Draft aspiration]
UNDENIABLE GAIN: [Draft outcomes]
STEP TO ACTION: [Draft next steps]
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

## Confirm & Refine

2-3 questions maximum:

1. **Does Scenario → Inflection → Status Quo create urgency?**
   - [ ] Yes / Adjust Scenario / Strengthen Inflection / Clarify Status Quo

2. **Does Insight → Approach → Proof establish credibility?**
   - [ ] Yes / Refine Insight / Sharpen Approach / Strengthen Proof

3. **Specific language, data, or examples to include?**
   - [ ] Complete / Add statistic / Add example / Emphasize point

## Output Format

Write to `/messaging/pitch.md`:

```markdown
# Messaging House - Pitch

Our pitch is our strategic company narrative — the story we tell end-to-end to explain why change is necessary and why we are uniquely positioned to lead it.

Use this section to bring storytelling into messaging and content assets.

## Messaging Blocks

### Strategic Narrative

**The Scenario**
[1-2 paragraphs: attention hook - current conditions facing audience]

**The Inflection**
[1 paragraph: industry forces making this urgent]

**The Status Quo**
[1 paragraph: why existing approaches fail despite attempts]

**Our Smart Insight**
[1 paragraph: what you figured out that others missed]

**Our Unique Approach**
[1-2 paragraphs: what you built and why it's different]

**Our Proof of Value**
[1 paragraph: tangible evidence - quotes, mentions, metrics]

**Reason to Believe**
[1 paragraph: what audience can advocate for]

**Undeniable Gain**
[1 paragraph: quantitative and qualitative outcomes]

**Step to Action**
[1 paragraph: tangible next steps tied to embracing change]

### Elevator Pitch

[2-4 sentences: conversational, assumes no context, all bangers no filler]

## Rules

- Do not repeat the full pitch unless explicitly instructed

## Guidelines

- Preserve the narrative logic, not the exact language
- Maintain the flow from market → company → buyer perspective
```

## Validation

- [ ] Checked `/research/` and all prior components
- [ ] Each element traces to a source component
- [ ] Scenario → Inflection → Status Quo creates urgency
- [ ] Insight → Approach → Proof establishes credibility
- [ ] Believe → Gain → Action inspires action
- [ ] Elevator Pitch is 30-60 seconds spoken, conversational
