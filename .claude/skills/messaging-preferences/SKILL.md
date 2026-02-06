---
name: messaging-preferences
description: Build the Preferences component of your Messaging House - the writing tone, style, voice, and guidelines that ensure consistency across all content.
---

# Messaging Preferences Builder

Build the **Preferences** - writing guardrails for all content.

**Blocks**: Technical Depth | Tone Style | Theme Pillars | Tips & Tricks | Tropes to Avoid

**Dependencies**: All prior components for style analysis

## Workflow

1. **LOAD ALL CONTEXT**
   Read all prior components → Analyze tone and style patterns
   Scan `/research/` → Look for brand guidelines, style guides

2. **ANALYZE PATTERNS**
   Extract tone indicators from Purpose, Pitch
   Note technical depth from People (personas)
   Identify themes from Position, Proposition

3. **RESEARCH (if needed)**
   Check company blog for existing voice

4. **PRESENT ANALYSIS**
   Show observed patterns and draft preferences

5. **CONFIRM & REFINE**
   User validates (5 questions)

6. **GENERATE**
   Create blocks → Write to `/messaging/preferences.md` → Validate

## Generation Approach

### Deriving Preferences from Prior Components

Preferences are **derived**, not invented. Extract patterns from what's already built:

| Block | Source | What to extract |
|-------|--------|-----------------|
| **Technical Depth** | People (personas) | Who are we speaking to? Executives or practitioners? |
| **Tone** | Purpose, Pitch | What's the narrative energy? Urgent? Confident? |
| **Themes** | Position, Proposition | What beliefs do we keep returning to? |
| **Language** | Pitch narrative | What sentence structure and word choice works? |

### Key Principle
**Tropes to Avoid takes precedence over all other stylistic guidance.** If something is on the avoid list, it doesn't get used regardless of other rules.

### Quality Filters

**Technical Depth:**
- What can be assumed known?
- What needs explanation?
- Default level should match primary persona

**Tone Style:**
- Formality: Very formal → Professional → Conversational → Casual
- Authority: Expert → Confident guide → Collaborative → Humble helper
- Energy: All business → Mostly serious → Balanced → Playful

**Theme Pillars:**
- Should emerge from Position and Proposition
- 3-5 core beliefs, not taglines
- Each should influence how you write, not what you write

**Tropes to Avoid:**
- Be specific, not generic ("leverage" is specific; "bad writing" is not)
- Include competitor language you don't want to use
- Include cliches common to your industry

## Present Analysis

```
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
PREFERENCES ANALYSIS
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

OBSERVED PATTERNS:

Technical Depth:
- Personas include: [list from People]
- Suggested default: [level]

Tone (from Purpose + Pitch):
- Vision tone: [observed]
- Narrative style: [observed]
- Suggested voice: [adjectives]

Theme Pillars (from Position + Proposition):
- Market stance: [belief]
- Value emphasis: [theme]
- Suggested pillars: [list]

DRAFT PREFERENCES:

Technical Depth: [level]
Formality: [Professional/Conversational/Casual]
Authority: [Expert/Guide/Collaborative]
Energy: [Serious/Balanced/Playful]

Theme Pillars:
1. [Belief from Position/Proposition]
2. [Belief from Purpose]
3. [Belief from differentiation]
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

## Confirm & Refine

5 questions maximum:

1. **Default technical depth?**
   - [ ] Executive/business
   - [ ] Technical leadership
   - [ ] Practitioner
   - [ ] Developer/engineer

2. **Brand voice?**
   Formality: Very formal / Professional / Conversational / Casual
   Authority: Expert / Confident guide / Collaborative
   Energy: All business / Mostly serious / Balanced / Playful

3. **Core beliefs (3-5)?**
   Suggested: [themes from analysis]
   - [ ] These capture us / Adjust / Add

4. **Language to avoid?**
   - [ ] Buzzwords: [terms]
   - [ ] Generic marketing: [examples]
   - [ ] Competitor language: [terms]

5. **Specific writing guidance?**
   - [ ] None needed / Add: [describe]

## Output Format

Write to `/messaging/preferences.md`:

```markdown
# Messaging House - Preferences

Preferences define writing tone, style, and voice.

## Technical Depth

[Default level. What can be assumed, what needs explanation.]

## Tone Style

[Overall vibe. Formality, authority, energy spectrum positions.]

## Theme Pillars

1. **[Theme 1]**: [How it influences messaging]
2. **[Theme 2]**: [Description]
3. **[Theme 3]**: [Description]

## Tips & Tricks

- [Tip 1]
- [Tip 2]
- [Tip 3]

## Tropes to Avoid

- [Trope 1]
- [Trope 2]
- [Trope 3]

## Rules

- Preferences are always-on unless explicitly overridden by a Skill
- Tropes to Avoid takes precedence over all other stylistic guidance
- Do not introduce stylistic elements that conflict with Tone Style or Theme Pillars

## Guidelines

- When in doubt, favor clarity, precision, and restraint
- Consistency of voice and clarity in message matters more than creativity
- Let insight and structure carry the message, not stylistic flair
```

## Validation

- [ ] Analyzed patterns from prior components
- [ ] Tone aligns with Purpose and Pitch
- [ ] Technical depth appropriate for personas
- [ ] Theme pillars distinct from competitors
- [ ] Tropes are specific, not generic
