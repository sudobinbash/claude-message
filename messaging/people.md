# Messaging House - People

The People defines our target audience with relevant characteristics nad behaviors to align messaging to.

Use this section to ensure precision and resonance. Messaging should only target audiences that meet ICP criteria, then be tailored by segment and persona when applicable.

## Messaging Blocks

### Ideal Customer Profile (ICP)

The ICP criteria defines good fit / bad fit accounts. 

#### Disqualifying Conditions

[Instructions:
State who this is not for and why. These constraints are as important as fit criteria.

Claude will use these conditions to explicitly avoid irrelevant scenarios.]

[Tips:
– Be honest and specific using quantitative and qualitative measures
– Disqualify based on current reality, not future ambition
– Messaging assumes present-day conditions, not hoped-for maturity]

[Format:
Bullet list of conditions that indicate bad fit accounts]

#### Characteristics

[Instructions:
Define the structural traits that make a company a strong fit right now. These should describe the kind of organization where the problem is real, visible, and funded.

Claude will use these attributes to tune scenarios and proof points to the right type of company.]

[Tips:
– Focus on structural realities (complexity, scale, regulations, operating model, etc.)
– Avoid vanity descriptors]

[Format:
Bullet list of defining traits]

#### Behaviors

[Instructions:
Describe observable behaviors that indicate active pain, urgency, or readiness. These should be signals that something is breaking, changing, or being prioritized.

Claude uses these signals to frame urgency and relevance.]

[Tips:
– Favor real actions over possible intent
– Look for signals tied to budget, risk, or operational strain]

[Format:
Bullet list of behaviors or signals]

#### Environment

[Instructions:
Describe the operational, technical, or organizational conditions the company operates under that matter to your solution.

Claude will use this to ensure messaging reflects the real-world constraints and trade-offs the audience faces.]

[Tips:
– Include people, process, and technology considerations
]

[Format:
Short paragraph or bullets describing environmental factors]

#### Maturity

[Instructions:
Define where good-fit customers typically are in their journey relative to this problem space. 

Claude will use this to calibrate depth, sequencing, and expectations in messaging.]

[Tips:
– Map specific levels to a maturity curve
– It's less about qualification and more about alignment]

[Format:
1–2 sentences describing typical stage of readiness]

### Customer Journey

The Customer Journey defines how messaging should evolve over time as the audience's awareness, evaluation, adoption, and advocacy evolve. 

[Instructions:
Document each stage of the customer journey from a messaging perspective. Focus on the intent, emotional shift, message emphasis, and proof emphasis that best move customers through each stage.

Claude will use journey stages to calibrate messaging depth, specificity, and proof. Earlier stages require framing and insight; later stages require confidence and validation.]

[Note: 
Keep this section focused on messaging that matters. You may have prescriptive marketing attribution measures, sales stages, and/or technical maturity phases.]

[Tips:
– Only craft focused messages that matters to this stage - avoid watering down consistent value messaging
- Internalize the "walk away feeling" to get a sense for how to move the customer from one phase to the next
- The journey applies to individual personas, teams, and the organization as a whole]

[Format:
For each journey stage, include:
- Primary Goal: describe your messaging intent when it comes to moving someone through this stage
- Walk Away Feeling: describe what the customer should be feeling that will move them through this stage
- Key Messaging: list any specific complementary messages that apply to this stage
- Best Proof: list the specific types of proof points that do best at this stage - with examples if you have them]

[Example Journey Stage:
Awareness

Goal
Make them care about the problem domain.

Walk Away Feeling
"Wow. Yes, that's a real pain point I’d like to solve."

Key Messages
(High-level problem framing, industry shifts, and consequences of inaction)

Proof Types
(Trends, insights, analogies, third-party perspectives)]

### Persona Profiles

Personas are the specific people we aim to speak directly to with our messaging - from executives to practitioners. 

When specific personas are related to your task workflow, extract the respective profile in `/messaging/personas/` for in-depth messaging.

| Persona   | File           | 
|-----------|----------------|
| Persona A | persona-a.md   |
| Persona B | persona-b.md   |
| Persona C | persona-c.md   |

[Instructions:
List the specific personas that apply to your GTM. Personas should be grounded in real responsibilities, pressures, and motivations. Avoid generic demographic or personality-based descriptions that have no impact to your solution. For each persona, carve out a distinct profile in `/messaging/personas/[persona-name].md`

Claude will use persona profiles to ensure messaging is relevant to pain points, wants, and needs, and flies at the right altitude in terms of the buying process.]

### Segment Profiles

Segments define company-level groupings that carry specific considerations beyond what is already covered across the ICP and core messaging elements.

When specific segments are related to your task workflow, extract the respective profile in `/messaging/segments/` for in-depth messaging.

| Segment   | File           | 
|-----------|----------------|
| Segment A | segment-a.md   |
| Segment B | segment-b.md   |
| Segment C | segment-c.md   |

[Instructions:
List specific company segments that carry particular messaging considerations. Only create Segments when you need additional contextual clarifiers - i.e. compliance regulations, regional differences, scale implications, etc. This isn't Segments for your territory planning, it's for your messaging. For each segment, carve out a distinct profile in `/messaging/segments/[segment-name].md`

Claude will use this section to customize messaging based on certain conditions that only apply to select segments.]

## Rules

- ICP defines eligibility — if ICP conditions are not met, assume no fit, urgency, or budget
- Validate ICP fit before refining to specific segments and personas
- Do not invent personas or segments beyond those defined

## Guidelines

- Use ICP signals to determine whether urgency is inferred or needs to be established
- Personas influence tone, direction, and value emphasis — not positioning
- Segments should adapt context and emphasis, not redefine value propositions or audience fit
