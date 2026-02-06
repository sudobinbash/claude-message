---
name: messaging-profile
description: Build the Company Profile element of your Messaging House - the foundational company facts, boilerplate statement, and marketplace description used for consistent external introductions.
---

# Messaging Profile Builder

Build the **Profile** - the factual foundation of who the company is.

**Blocks**: Foundation | Boilerplate Statement | Marketplace Statement

**First in sequence** - provides context for all other components.

## Workflow

1. **GET COMPANY NAME**
   Ask: "What company are we building the Profile for?"

2. **LOAD LOCAL RESEARCH**
   Scan `/research/` → Summarize available content → Note gaps

3. **RESEARCH GAPS**
   WebSearch only for missing info: about, funding, customers, press, G2

4. **PRESENT FINDINGS**
   Show discovered info → Highlight gaps needing input

5. **CONFIRM & REFINE**
   User validates facts → Fills gaps (4 questions max)

6. **GENERATE**
   Create blocks → Write to `/messaging/profile.md` → Validate

## Research

### Priority Order
1. Scan `/research/` for company info
2. WebSearch only for gaps

### Queries (if needed)
| Query | Purpose |
|-------|---------|
| `"{company} about"` | Description, market category |
| `"{company} crunchbase"` | Funding, investors, founding |
| `"{company} customers"` | Notable customers, count |
| `"{company} press release"` | Existing boilerplate |
| `"{company} G2"` | Marketplace description |

### Extract
- Identity: description, market category, what they do
- Scale: employees, customers, funding stage
- Credibility: investors, notable customers
- Existing copy: press boilerplate, G2 description

## Generation Approach

### Foundation
A fact sheet for reference - type, market, founding, investors, customers, regions, verticals, compliance, size.

**How to generate:**
- Neutral, reference tone - no narrative or positioning
- Include only verified or user-confirmed facts
- Keep it practical: this is lookup, not storytelling

**Format:** Bulleted list with labeled fields

### Boilerplate Statement
Canonical "About" copy reusable verbatim across press releases, social profiles, partner listings.

**How to generate:**
- Write in third person
- Keep it concise and authoritative (2-4 sentences, 50-75 words)
- Avoid campaign-specific phrasing or time-bound claims
- State what the company does, who it serves, and why it matters

**Quality filter:** Could this appear unchanged in a press release footer?

### Marketplace Statement
Product-focused description for listings - more outcome-oriented than boilerplate.

**How to generate:**
- Emphasize primary use cases and measurable business outcomes
- Use clear, accessible language aligned to buyer expectations
- Avoid exaggerated claims, competitive language, or narrative framing

**Format:** 1-2 sentences intro + 3-5 bullet points

## Output Format

Write to `/messaging/profile.md`:

```markdown
# Messaging House - Profile

Our Profile is the foundation of who we are as a company, tuned for various distribution channels.

Use this section to introduce the company accurately and consistently in external settings.

## Messaging Blocks

### Foundation

- **Company Type:** [type]
- **Market Space:** [category]
- **Founded:** [year]
- **Headquarters:** [location]
- **Funding/Investors:** [if relevant]
- **Customer Base:** [if public]
- **Supported Regions:** [markets]
- **Target Verticals:** [industries]
- **Compliance:** [frameworks]
- **Company Size:** [range]

### Boilerplate Statement

[2-4 sentences, third person, 50-75 words]

### Marketplace Statement

[1-2 sentence intro]

**Key Capabilities:**
- [Use case with outcome]
- [Use case with outcome]
- [Use case with outcome]

## Usage Guidelines

- Use Foundation when company facts are required
- Use Boilerplate for formal or press-style introductions
- Use Marketplace for listings, catalogs, and partner directories
- Do not introduce differentiation, unique POV, or belief with this layer
```

## Validation

- [ ] Checked `/research/` before searching
- [ ] Facts verified or user-confirmed
- [ ] Boilerplate: third person, 50-75 words, no time-bound claims
- [ ] Marketplace: outcome-oriented, practical language
- [ ] Reused existing copy where available
