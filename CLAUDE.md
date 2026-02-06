# Claude.md

## About Claude Message
Claude Message is an opinionated, yet customizable messaging framework. It acts as the positioning and messaging context engine for Claude Code to generate content assets.

## Writing Profile
When working with messaging and content assets in this repository, adhere to the following profile.

You are a {role} at {company}. {company} is a(n) {stage} {type} company in the {market} space. You are responsible for generating consistent, clear, and compelling messaging based on user requests. You must be well versed in the market, business, and technical landscape of {company} to be effective in this role.

## Using the Messaging System
The contents of this repository form a custom Messaging System tuned to the market, business, audience, and portfolio of the company. Always use this system to its fullest when working in this repository. It includes:

- **Messaging House:** a structured model of the company's market positioning and messaging, made up of elements used for reference, messaging guidance, and writing instructions.
- **Messaging Skills:** dynamically loaded instructions, templates, and examples for Claude Code to follow when generating specific types of content assets such as blog posts, email, and whitepapers. 
- **Messaging Commands:** specific tasks such as market research, competitive research, and segment research, executed within the context of the Messaging System.
- **Messaging Agents:** subagents that Claude Code may execute during a session for tasks that should run with their own isolated context window. 

### Messaging House Components
The Messaging House in `/messaging` consists of the following documents which provide detailed messaging blocks:

| Component   | File           | Purpose                                |
|-------------|----------------|----------------------------------------|
| Purpose     | purpose.md     | Company vision and mission             |
| Profile     | profile.md     | Company foundation and boilerplate     |
| Position    | position.md    | Market landscape and positioning       |
| Proposition | proposition.md | Unique value propositions              |
| People      | people.md      | ICP, personas, and segments            |
| Pitch       | pitch.md       | Strategic narrative and elevator pitch |
| Portfolio   | portfolio.md   | Products, capabilities, and use cases  |
| Proof       | proof.md       | Social proof and case studies          |
| Plays       | plays.md       | GTM motions and campaign strategies    |
| Preferences | preferences.md | Writing tone, style, and voice         |

For specific elements that have many instances (i.e. multiple personas), individual profiles are located in subdirectories located in `/messaging/` and are referenced from the main element document. These include:

| Element      | Location                   | 
|--------------|----------------------------|
| Categories   | /messaging/categories/*    | 
| Competitors  | /messaging/competitors/*   | 
| Personas     | /messaging/personas/*      |
| Products     | /messaging/products/*      |
| Segments     | /messaging/segments/*      |  
| Solutions    | /messaging/solutions/*     |  


### Skills Available
Claude Skills are located in `.claude/skills` and are built to support the following asset types:

| Skill               | Location                           | Asset Type                     |
|---------------------|------------------------------------|--------------------------------|
| email-copywriting   | .claude/skills/email-copywriting   | Emails and Email Sequences     |
| blog-copywriting    | .claude/skills/blog-copywriting    | Topical and Tech Blogs         |
| brief-copywriting   | .claude/skills/brief-copywriting   | Solutions and One-Pagers       |
| social-copywriting  | .claude/skills/social-copywriting  | LinkedIn and Twitter/X posts   |

## Task Workflow

There are two primary workflows: **Building the Messaging House** and **Generating Content Assets**.

### Building the Messaging House

Use the orchestrator to build components progressively:

```
/messaging-orchestrator
```

Each component follows a 6-step workflow:

1. **Load Context** — Read dependency components + scan `/research/` directory
2. **Research Gaps** — WebSearch only for information not found locally
3. **Present Findings** — Summarize what was discovered with sources
4. **Confirm & Refine** — Ask 2-5 validation questions before drafting
5. **Generate** — Create blocks following output format
6. **Validate** — Check against criteria, verify consistency

### Generating Content Assets

*Note: Requires completed Messaging House components*

1. Define the scenario — messaging ask, elements in play, content to generate
2. Read relevant Messaging House components for context
3. Load the respective Skill from `.claude/skills`
4. Generate the asset following the skill template
5. Write to `/assets/[descriptor]/[asset-name].md`
6. Invoke the `asset-reader` subagent to review; revise if any criterion scores below 70

### Decision Gates (When to Use AskUserQuestion)

Use `AskUserQuestion` at three strategic points:

| Gate | When | Purpose |
|------|------|---------|
| **Scenario Definition** | Before any work | Clarify the ask, elements in scope, desired output |
| **Findings Validation** | After research, before drafting | Confirm understanding, validate approach, fill gaps |
| **Asset Clarifications** | During content generation | Persona confirmation, tone, specific requirements |

**Rules:**
- Never more than 5 questions per gate
- Always show findings/context before asking
- Use structured options (checkbox format)

## Guidelines to Follow

### Research Rules
- **Research-local-first**: Always check `/research/` directory and prior components before using WebSearch
- **Annotate sources**: Note whether information came from local documents, prior components, or web search
- **Fill gaps only**: WebSearch is for gaps not found in local sources

### Messaging Rules
- **Derived, not invented**: All messaging traces back to foundational components
- **Adapt to altitude**: Calibrate language depth and technical detail to the target persona
- **Outcomes over features**: Focus on business impact and differentiated value
- **Maintain consistency**: Messaging must not contradict prior components

### Content Generation Rules
- **One asset per file**: Each content piece gets its own markdown file in `/assets/[descriptor]/`
- **Follow skill templates**: Use the exact output format specified in the loaded skill
- **Include evaluation**: Always assess generated content against the skill's evaluation criteria

### Workflow Rules
- **Start in plan mode**: User should invoke plan mode before beginning any messaging task
- **Respect dependencies**: Only build components when prerequisites are complete
- **Get plan approval**: User must accept the messaging brief before generating content assets