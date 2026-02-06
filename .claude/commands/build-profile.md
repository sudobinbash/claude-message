---
description: Build detailed element profiles for personas, products, solutions, categories, competitors, or segments
tags: [messaging, elements]
---

# Build Element Profile

Create detailed profiles for specific elements referenced in the Messaging House.

## Usage

```
/build-profile [element-type] [element-name]
```

## Element Types

| Type | Location | Parent Component |
|------|----------|------------------|
| persona | `/messaging/personas/{slug}.md` | People |
| segment | `/messaging/segments/{slug}.md` | People |
| product | `/messaging/products/{slug}.md` | Portfolio |
| solution | `/messaging/solutions/{slug}.md` | Portfolio |
| category | `/messaging/categories/{slug}.md` | Position |
| competitor | `/messaging/competitors/{slug}.md` | Position |

## Workflow

1. **ASK ELEMENT TYPE** (if not provided)
   Which element type? persona / segment / product / solution / category / competitor

2. **ASK ELEMENT NAME** (if not provided)
   What is the name of this [element-type]?

3. **LOAD CONTEXT**
   - Read relevant messaging components:
     - Persona/Segment → Read People, Profile
     - Product/Solution → Read Portfolio, Profile
     - Category/Competitor → Read Position, Profile
   - Scan `/research/` for related content

4. **RESEARCH**
   - WebSearch for element-specific information
   - Extract relevant data points

5. **GENERATE PROFILE**
   - Use template below
   - Create profile in appropriate directory

6. **UPDATE PARENT**
   - Add reference to parent component table

## Templates

### Persona (`/messaging/personas/{slug}.md`)

```markdown
# {Persona Name}

[Tips:
– A useful mental model is to ask what this person is "on the hook for" and what they are "on the hunt for".
- Frame value messaging as: Current State → Desired State → How to Get There → Why Only Us]

## Attributes

- Job Titles: [List of relevant titles]
- Role in the Buying Process: [Executive Buyer, Buyer, Champion, Influencer, Detractor]
- Role in the Product: [Owner, Administrator, End User, Observer]

## Roles & Responsibilities
[1-2 sentences with bullet points that define what this persona owns, influences, and is accountable for. Keep this practical and jobs-to-be-done oriented.]

## Relevant Signals
[1-2 sentences with bullet points that describe the conditions, behaviors, or buying patterns that indicate this persona is motivated to act.]

## Value Messages
[3-5 specific messages that consistently resonate with this specific persona.]

## Potential Objections
[1-2 sentences with bullet points that surface common objections this persona typically has in context of your solution.]
```

### Product (`/messaging/products/{slug}.md`)

```markdown
# {Product Name}

[Tips:
– Include context that is relevant to messaging, not every product detail
- Be explicit and clear about what the product is capable of
- Focus value messaging on what's truly differentiated]

## Attributes

- Type: [Platform, Product, Add-On, Module, Service]
- Lifecycle: [Early Access, Beta, Generally Available, Discontinued]
- Web Link: [optional]
- Documentation: [optional]

## Product Overview
[1-2 paragraphs explaining what the product does and who it's for]

## Positioning Statement
[1-2 sentences that dictate how this product fits in the market]

## Critical Capabilities
[Expanded bullet points detailing the most critical capabilities that drive value for this product – it's not a feature matrix]

## Technical Details
[More in-depth details about how it works, how it's deployed, etc.]

## Value Messages
[3-5 specific messages that convey why your product is different than the rest, and what unique value it delivers]
```

### Solution (`/messaging/solutions/{slug}.md`)

```markdown
# {Solution Name}

[Tips:
– Aim for solutions that are both hands-on practical for practitioners and valuable to the business
- When you have a lot of use cases, try to logically group them to avoid messaging sprawl]

## Attributes

- Scope: [Organizational, Department, Team, Cross-Functional, Individual]
- Theme: [Efficiency, Savings, Growth, Compliance, Replacement]
- Measures: [Less Time, More Revenue, Lower Costs, Faster Performance, etc.]
- Applicable Products: [Product A, Product A + B, etc.]

## Solution Description
[1-2 paragraphs explaining the scenario, the problem to solve, and the desired outcome]

## Unique Approach
[1-2 sentences with expanded bullet points that describe your answer]

## Value Messages
[3-5 specific messages that convey why your solution is different than the rest, and what unique value it delivers]
```

### Category (`/messaging/categories/{slug}.md`)

```markdown
# {Category Name} ({Acronym})

[Tips:
– Be clear about direct and adjacent positioning
- It's okay for there to be a proverbial venn diagram - this is for context
– Be honest about your relative position - this isn't a pitch]

## Attributes

- Maturity: [Emerging, Growing, Peak, Declining, Established]
- Coverage: [Broad, Specialized]
- Related Categories: [Adjacent, Converging, Consolidating]

## Category Overview
[1-2 sentence description of the category]

## Our Solution
[1-2 sentence description of your solution]

## Current Position
[1 sentence statement with relative position – Outside, New Entrant, Visionary, Challenger, Leader]

## Strategic Aim
[1 sentence statement with the end goal - Lead, Differentiate, Converge, Consume]
```

### Competitor (`/messaging/competitors/{slug}.md`)

```markdown
# {Competitor Name}

[Tips:
– Focus messaging on what's uniquely yours
- Keep the SWOT focused on things relevant to messaging
- Aim to keep this section fresh with the latest research]

## Attributes

- Type: [Vendor, DIY, Inaction]
- Current Position: [Emerging, Visionary, Challenger, Leader]
- Our Approach: [Beat, Differentiate, Cooperate, Target, Monitor]

## Description
[1-2 short paragraphs explaining the alternative solution and why customers may choose them over you]

## SWOT Analysis
[1-2 sentences with bullet points for each theme - not as the goto battlecard, rather what goes into messaging]

## Why Customers Choose Us
[1-2 short paragraphs detailing your competitive advantage]

## Differentiation Messages
[2-3 brief statements that focus on what makes you different - i.e. "unlike X, we..."]
```

### Segment (`/messaging/segments/{slug}.md`)

```markdown
# {Segment Name}

[Tips:
– Call out why a specific segment-based attribute matters when crafting messaging
– Segments should be additive to ICP, not duplicative]

## Attributes

- Verticals: [Technology, Retail, Telecommunications, Financial Services, etc.]
- Regions: [Global, Regional]
- Company Size: [# of Employees]

## Relevant Characteristics
[1-2 sentences with bullet points that describe the specific conditions that materially affect messaging in this segment. Focus on constraints, risks, or priorities that differ from the ICP baseline.]

## Relevant Behaviors
[1-2 sentences with bullet points that describe the observable, company-level signals that indicate a consideration where messaging should be adapted]

## Value Messages
[3-5 specific messages that consistently resonate with companies in this specific segment]

## Potential Objections
[1-2 sentences with bullet points that surface common objections companies in this segment typically have in context of your solution.]
```

## Research Queries by Type

| Type | Queries |
|------|---------|
| Persona | `"{title} responsibilities"`, `"{title} challenges"` |
| Product | `"{company} {product}"`, `"{product} features"` |
| Solution | `"{company} {use case}"`, `"{problem} solutions"` |
| Category | `"{category} Gartner"`, `"{category} market"` |
| Competitor | `"{competitor} vs"`, `"{competitor} positioning"` |
| Segment | `"{industry} {market category}"` |

## Output

After generating the profile:
1. Write to `/messaging/{type}s/{slug}.md`
2. Update the parent component's reference table
3. Report what was created
