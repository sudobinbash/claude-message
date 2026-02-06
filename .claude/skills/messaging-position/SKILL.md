---
name: messaging-position
description: Build the Position component of your Messaging House - the market landscape, positioning statement, and competitive context that define where you stand.
---

# Messaging Position Builder

Build the **Position** - your market space and competitive context.

**Blocks**: Market Landscape | Positioning Statement | Categories | Alternatives

**Dependencies**: Profile, Purpose, Portfolio, Proposition → differentiation and value context

## Workflow

1. **LOAD CONTEXT**
   Read prior components → Extract: company, market, products, value props
   Scan `/research/` → Look for market/competitive content

2. **RESEARCH GAPS**
   WebSearch (if needed): market trends, analyst coverage, competitors

3. **PRESENT FINDINGS**
   Show market landscape, categories, competitors found

4. **CONFIRM & REFINE**
   User validates landscape, provides differentiation (4-5 questions)

5. **GENERATE**
   Create blocks → Write to `/messaging/position.md` → Validate

## Research

### Priority Order
1. Scan `/research/` for market/competitive content
2. Read prior components (especially Proposition for differentiation)
3. WebSearch only for gaps

### Queries (if needed)
| Query | Purpose |
|-------|---------|
| `"{market category} market trends 2026"` | Market forces |
| `"{market category} Gartner"` | Analyst landscape |
| `"{company} competitors"` | Who they're compared to |
| `"{company} vs"` | Direct comparisons |

### Extract
- Market forces: technology shifts, regulatory, economic
- Trends: industry direction, hype cycles
- Categories: analyst-defined segments
- Competitors: direct, adjacent, DIY alternatives

## Generation Approach

### Market Landscape
Write an **opinionated view** of the market - not a neutral summary.

**How to generate:**
- Anchor on market forces shaping buyer behavior (tech shifts, regulations, economic)
- Speak to industry trends (movements, hype cycles, consolidation)
- Introduce YOUR perspective on where the market is headed
- Take a stance that sets up your differentiation

**Quality filter:** Would a competitor disagree with this take?

### Positioning Statement
Use the Gartner framework but don't copy it verbatim in content.

**How to generate:**
- Pull `For` and `Who` from Profile audience
- Pull `That` (key benefit) from Proposition one-liners
- `We` and `Only Us` come from Proposition differentiation
- `With Us` is the primary gain

**Reference:** April Dunford's "Obviously Awesome" for positioning depth.

### Categories & Alternatives
Be honest about relative position - this is context, not a pitch.

**How to generate:**
- Categories: Use analyst terminology (Gartner, Forrester)
- Competitors: Include vendors, DIY, and inaction
- Link to profiles in `/messaging/categories/` and `/messaging/competitors/`

## Present Findings

```
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
RESEARCH FINDINGS: POSITION
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

CONTEXT:
- Company: {company_name}
- Market: {market_category}
- Key Differentiation: {from Proposition}

MARKET LANDSCAPE:
Key forces: [technology shifts, regulatory, etc.]
Trends: [industry direction]

CATEGORIES FOUND:
- {category} (Gartner/Forrester)

COMPETITORS FOUND:
Direct: [competitors]
Adjacent: [solutions]

GAPS (need input):
- Your unique market perspective
- Specific differentiation claims
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

## Confirm & Refine

4-5 questions maximum:

1. **Market landscape accurate?**
   - [ ] Yes / Additions: [describe]

2. **What's your unique market perspective?**
   - [ ] We believe [assumption] is wrong
   - [ ] We see a shift others miss
   - [ ] We prioritize [X] over [Y]

3. **Competitors and categories correct?**
   - [ ] Yes / Missing: [add] / Incorrect: [correct]

4. **Primary differentiation?**
   Unlike alternatives, you: [describe]

5. **Primary gain customers achieve?**
   With you, customers: [describe outcome]

## Output Format

Write to `/messaging/position.md`:

```markdown
# Messaging House - Position

Our Position is our market space and the competing alternatives we go up against.

Use this section when performing market and competitive research. Also use this section to ensure messaging is relevant to industry trends and clearly differentiated.

## Messaging Blocks

### Market Landscape

[2-3 paragraphs: market forces, trends, your unique perspective on direction]

### Positioning Statement

- **For** [Target Audience]
- **Who** [Statement of Need]
- **And Want** [Statement of Expectations]
- **We are** [Primary Position / Category]
- **That** [Statement of Key Benefit]
- **Unlike** [Alternatives]
- **We** [Primary Differentiation]
- **Only Us** [Unique Approach]
- **With Us** [Primary Gain]

### Categories in Play

When researching categories, extract from `/messaging/categories/`.

| Category | Source Files |
|----------|--------------|
| [Category] | category-name.md |

### Competing Alternatives

When researching alternatives, extract from `/messaging/competitors/`.

| Alternative | Source Files |
|-------------|--------------|
| [Competitor] | competitor-name.md |

## Rules

- Positioning statement anchors differentiation, not verbatim copy
- No competitive attacks - describe alternatives fairly

## Guidelines

- Market landscape takes a stance
- Test positioning against alternatives
- Balance vision with reality
```

## Validation

- [ ] Checked `/research/` before searching
- [ ] Market landscape has 2-3 paragraphs with a stance
- [ ] Positioning statement built from Proposition differentiation
- [ ] Differentiation is clear vs. alternatives
- [ ] Categories use industry-standard terminology
