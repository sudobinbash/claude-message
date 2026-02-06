---
name: messaging-proof
description: Build the Proof component of your Messaging House - the tangible evidence that validates your narrative, positioning, and value propositions.
---

# Messaging Proof Builder

Build the **Proof** - evidence that your claims are real.

**Blocks**: Value Measures | Customer Stories | Analyst Mentions | Community Love

**Dependencies**: Profile, Portfolio, People, Proposition

## Workflow

1. **LOAD CONTEXT**
   Read prior components → Extract: customers, products, personas, value props
   Scan `/research/` → Look for case studies, testimonials, analyst content

2. **RESEARCH GAPS**
   WebSearch (if needed): case studies, ROI, G2 reviews, analyst coverage

3. **PRESENT FINDINGS**
   Show proof by category, identify gaps

4. **CONFIRM & REFINE**
   User validates, adds internal data (4 questions)

5. **GENERATE**
   Create blocks → Write to `/messaging/proof.md` → Validate

## Research

### Priority Order
1. Scan `/research/` for proof content (case studies, reviews, analyst)
2. Read prior components for context
3. WebSearch only for gaps

### Queries (if needed)
| Query | Purpose |
|-------|---------|
| `"{company} case studies"` | Customer stories |
| `"{company} ROI"` | Value metrics |
| `"{company} G2 reviews"` | Community sentiment |
| `"{company} Gartner"` | Analyst recognition |

### Extract
- Value Measures: % improvement, time saved, cost reduced
- Customer Stories: company, industry, outcomes, quotes
- Analyst Mentions: reports, recognitions, placements
- Community Love: ratings, praise themes, notable quotes

## Generation Approach

### Matching Proof to Journey Stage
Different proof works at different stages:

| Stage | Best Proof Types |
|-------|------------------|
| **Awareness** | Trends, third-party perspectives, analyst insights |
| **Consideration** | Industry stats, peer validation, "people like me" |
| **Evaluation** | Case studies, demos, technical validation |
| **Decision** | ROI calculators, references, risk reduction |

### Quality Filters

**Value Measures:**
- Focus on outcomes, not activity
- Specific > generic ("40% faster" > "significant improvement")
- Include context (scenario, timeframe, baseline)

**Customer Stories:**
- Must be publicly referenceable OR properly anonymized
- Include the "why" (compelling event that led to action)
- Quote should be pull-out worthy

**Analyst Mentions:**
- Include date and context (report, category)
- What does the recognition imply?

**Community Love:**
- Look for patterns across reviews, not just individual quotes
- What themes emerge?

## Present Findings

```
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
RESEARCH FINDINGS: PROOF
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

VALUE MEASURES:
- [Metric 1]: [X% improvement]
- [Metric 2]: [X hours saved]

CUSTOMER STORIES:
| Customer | Industry | Outcome |
|----------|----------|---------|
| [Name] | [Industry] | [Result] |

ANALYST MENTIONS:
- [Firm]: [Report - Date]

COMMUNITY LOVE:
- Rating: [X/5 on G2]
- Themes: [common praise]
- Quote: "[notable quote]"

GAPS:
- [e.g., no public ROI metrics]
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

## Confirm & Refine

4 questions maximum:

1. **Value measures accurate?**
   - [ ] Yes / Add internal metrics / Corrections

2. **Customer stories referenceable?**
   - [ ] Yes, all public / Some confidential / Add stories

3. **Analyst coverage complete?**
   - [ ] Yes / Add recognition / Correct date/context

4. **Community proof complete?**
   - [ ] Yes / Add source / Add notable quote

## Output Format

Write to `/messaging/proof.md`:

```markdown
# Messaging House - Proof

The Proof provides evidence that our claims are real.

## Messaging Blocks

### Business Value Measures

**[Metric/Direction]**
- Description: [Supporting value message]
- Context: [Where/when this applies]
- Source: [How you know this]

---

### Customer Stories

**[Customer Name or Anonymous]**
- Profile: [Industry, size, region]
- Scenario: [Conditions that led to you]
- Why They Acted: [Compelling event]
- Outcome: [Quantitative and qualitative]
- Quote: "[Pull-out statement]"

---

### Analyst Mentions

**[Analyst Firm]**
- Context: [Report, category, date]
- Key Takeaway: [What recognition implies]

---

### Community Love

**[Source Type]**
- Theme: [What pattern it represents]
- Example: "[Quote or summary]"

---

## Rules

- Proof supports claims, doesn't create them
- Select proof appropriate to audience and journey stage
- If proof is weak, avoid overconfident claims

## Guidelines

- Match proof type to intent (metrics for justification, stories for relatability)
- Increase proof strength as buyer journey progresses
- Prefer specificity over logos
```

## Validation

- [ ] Checked `/research/` before searching
- [ ] Value measures focus on outcomes, not activity
- [ ] Customer stories are publicly referenceable or anonymized
- [ ] Analyst mentions include context and date
- [ ] Community proof shows patterns, not just quotes
