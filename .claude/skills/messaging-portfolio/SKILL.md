---
name: messaging-portfolio
description: Build the Portfolio component of your Messaging House - the products, capabilities, and solutions that define what you offer and how it's structured.
---

# Messaging Portfolio Builder

Build the **Portfolio** - what you offer and how it's structured.

**Blocks**: Portfolio Overview | Product Details | Solutions

**Dependencies**: Profile, Purpose → company_name, market_category, vision, mission

## Workflow

1. **LOAD CONTEXT**
   Read Profile, Purpose → Extract: company_name, market_category, vision, mission
   Scan `/research/` → Look for product/solution content

2. **RESEARCH GAPS**
   WebSearch (if needed): products, pricing, solutions, features, integrations

3. **PRESENT FINDINGS**
   Show portfolio structure, products found, solutions found

4. **CONFIRM & REFINE**
   User validates structure, products, solutions (3-4 questions)

5. **GENERATE**
   Create blocks → Write to `/messaging/portfolio.md` → Validate

## Research

### Priority Order
1. Scan `/research/` for product/solution content
2. Read Profile and Purpose
3. WebSearch only for gaps

### Queries (if needed)
| Query | Purpose |
|-------|---------|
| `"{company} products"` | Product pages |
| `"{company} pricing"` | Reveals structure/tiers |
| `"{company} solutions"` | Use cases |
| `"{company} features"` | Capabilities |

### Extract
- Structure: single product? multi-product? platform? modules?
- Products: names, descriptions, types (core/add-on)
- Solutions: use cases, jobs-to-be-done, outcomes
- Relationships: bundled, tiered, standalone

## Generation Approach

### Portfolio Overview

Write a structural overview that establishes **altitude** for messaging.

**How to generate:**
- Determine offering type: single product, multi-product, platform, or hybrid
- Map relationships: core vs add-on, bundled vs standalone, platform vs application
- Focus on structure, not features

**Quality filter:** Does this help decide when to speak at platform vs product level?

**Format:** 1 paragraph describing structure and relationships

### Product Details

Reference individual product profiles—don't duplicate content here.

**How to generate:**
- Create profiles in `/messaging/products/` for each canonical offering
- Include only messaging-relevant context (not feature matrices)
- Focus differentiated value, not comprehensive specifications

**Quality filter:** Would a salesperson use these profiles to position against competitors?

**Format:** Reference table linking to `/messaging/products/` profiles

### Solutions

Document outcome-oriented use cases that anchor business and technical value.

**How to generate:**
- Start with jobs-to-be-done: what are customers trying to accomplish?
- Solutions may span multiple products or apply to a single product
- Group logically to avoid messaging sprawl
- Ground in measurable outcomes, not product capabilities

**Quality filter:** Is this both hands-on practical for practitioners AND valuable to the business?

**Format:** Reference table linking to `/messaging/solutions/` profiles

## Output Format

Write to `/messaging/portfolio.md`:

```markdown
# Messaging House - Portfolio

The Portfolio defines what we offer and how it is structured.

Use this section to understand the shape, hierarchy, and scope of our offerings so messaging stays at the correct altitude and references the right products and solutions at the right time.

## Messaging Blocks

### Portfolio Overview

[1 paragraph: structure and relationships. Single/multi-product? Platform? Add-ons?]

### Product Details

Products are the canonical units of offering within the portfolio.

When specific products are related to your task, extract the profile in `/messaging/products/`.

| Product | File |
|---------|------|
| [Product A] | product-a.md |

### Solutions

Solutions are the use cases of the product in practice.

When specific solutions are related to your task, extract the profile in `/messaging/solutions/`.

| Solution | File |
|----------|------|
| [Solution A] | solution-a.md |

## Rules

- Portfolio defines altitude — use it to speak broadly about the offering
- Products define scope — introduce them only when specificity is required
- Capabilities justify value — use them to explain why outcomes are achievable
- Technical details support credibility — include them selectively and last

## Guidelines

- Avoid long feature lists; introduce capabilities sparingly when they're additive
- Prefer buyer outcomes and use cases over product mechanics
- Elevate product value to meaningful, measurable business or technical impact
```

## Validation

- [ ] Checked `/research/` and prior components before searching
- [ ] Portfolio structure clear (platform vs. product)
- [ ] Products are canonical offerings
- [ ] Solutions are outcome-oriented
- [ ] Relationships between products understood
