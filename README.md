```
 _____ _                 _       ___  ___                               
/  __ \ |               | |      |  \/  |                               
| /  \/ | __ _ _   _  __| | ___  | .  . | ___  ___ ___  __ _  __ _  ___ 
| |   | |/ _` | | | |/ _` |/ _ \ | |\/| |/ _ \/ __/ __|/ _` |/ _` |/ _ \
| \__/\ | (_| | |_| | (_| |  __/ | |  | |  __/\__ \__ \ (_| | (_| |  __/
 \____/_|\__,_|\__,_|\__,_|\___| \_|  |_/\___||___/___/\__,_|\__, |\___|
                                                              __/ |     
                                                             |___/      
```

Claude Message is an opinionated, yet customizable messaging framework built around the Claude Code harness. It acts as the positioning and messaging context engine for Claude Code to generate content assets – ensuring the copy always strikes a chord and is uniquely yours.

This is meant for Product Marketers, Founders, and anyone who cares about messaging quality and taste. It's built primarily for B2B companies, but the principles may apply to others.

A basic understanding of how to use Claude Code, and how its harness works is required.

The tl;dr - fork it, tune to your market, write to your message, generate dope content. 

*I said who's house? Your house!*

## Getting Started

Claude Message requires in-depth messaging across a number of components. You can inspect the files with instructions in `/messaging` to customize, or run a progressive workflow that will bootstrap the system.

Run the orchestrator to guide you through:

```
/messaging-orchestrator
```

The orchestrator grabs existing messaging documents, performs outside research, and asks questions in a sequence – while tracking what's complete and recommends what to build next. Components are built in a predefined sequence to get the facts, the foundation, and the flair in the right order:

```
Profile → Purpose → Portfolio → Proposition → Position → Pitch → People → Proof → Preferences
```

Once your Messaging House is complete, the system will use your positioning and messaging as the context engine for content generation.

## How it Works

This repository is your messaging system for creating clear and compelling content tuned to your market. Your business is dynamic, your messaging must be too.

### Messaging House

The Messaging House is a structured model of your positioning and messaging. Components are built progressively—each one extracts context from prior components and adds new context for what comes next.

| # | Component | Purpose | Depends On |
|---|-----------|---------|------------|
| 1 | Profile | Company facts and foundation | — |
| 2 | Purpose | Vision and mission | Profile |
| 3 | Portfolio | Products and solutions | Profile |
| 4 | Proposition | Unique value | Profile, Purpose, Portfolio |
| 5 | Position | Market landscape | All prior |
| 6 | Pitch | Strategic narrative | All prior |
| 7 | People | Target audience | Profile, Portfolio, Proposition, Position |
| 8 | Proof | Evidence of value | Proposition, Profile |
| 9 | Preferences | Brand voice | All prior (derived) |

Within the components, there are specific elements that may contain multiple profiles. Carve out dedicated profiles for:

- Categories
- Competitors
- Personas
- Products
- Segments
- Solutions

### Messaging Skills

Messaging Skills are dynamically loaded instructions for Claude Code to follow when generating content assets. The Skills are focused on specific asset-types, and include a messaging brief, writing instructions, context pointers, guidelines to follow, evaluation criteria, and an output format template. The examples in this repository include:

- Email Copywriting
- Social Copywriting
- Blog Copywriting
- Brief Copywriting

### Messaging Commands

Messaging Commands are specific research tasks you can kick off from the Claude Code CLI. These tasks are executed within the context of the Messaging System, so they are naturally framed and pointed in the right direction. The examples in this repository include:

- Competitive Research
- Initiative Research
- Market Research
- Persona Research
- Segment Research

### Messaging Agents

Messaging Agents are subagents that Claude Code may execute during a session. Their advantage is having an isolated context window to perform a specific task without overwhelming the main session context window. I only included one subagent in this repo because I'm of the mindset that you only need to carve out subagents when you're testing the limits of the context window. For messaging and content generation, this is rarely an issue. If you find yourself hitting a wall, you can add more agents - just be sure to modify Claude.md to call the subagents during the task workflow.

I added an `asset-reader` subagent that reads and grades each generated asset after its written. This is an example of a clean context window being beneficial because there's no preconceived notion of what went into the content, just a persona-led response to what was generated. A good sniff test.

## Using This Repository

Fork this repository or copy the contents into your own Claude Code environment.

### Step 1: Add Your Research

Drop existing messaging documents into the `/research/` directory. The system will scan this folder first before searching externally. Include anything you have:

- Pitch decks and sales presentations
- Existing positioning documents
- Competitor analysis
- Customer research or interview notes
- Product briefs or PRDs

### Step 2: Configure Your Writing Profile

Edit `CLAUDE.md` to set your writing profile—role, company, stage, and market. This shapes how Claude approaches all messaging work.

### Step 3: Build Your Messaging House

Run the orchestrator to build components progressively:

```
/messaging-orchestrator
```

The orchestrator will guide you through each component in sequence, extracting from your research documents, asking clarifying questions, and generating structured output.

Alternatively, edit the markdown files in `/messaging/` directly. Each file includes instructions, tips, and format guidance for each block.

### Step 4: Generate Content

Once your Messaging House is complete, use Skills to generate assets:

```
/email-copywriting
/social-copywriting
/blog-copywriting
/brief-copywriting
```

Content will automatically inherit your positioning, voice, and messaging.

### Optional: Customize Skills and Commands

Review `.claude/skills/` to customize output formats, evaluation criteria, or add your own examples. Review `.claude/commands/` to adjust research task instructions. 

## Your Writing Profile

You can't change the main Claude Code system prompt, but you can provide a profile to guide its writing style. It's recommended to provide Claude Code with a more personal writing profile, rather than some generic, "you are a writing agent."

The default format provided in the sample `CLAUDE.md` file follows this structure:

```
You are a {role} at {company}. {company} is a(n) {stage} {type} company in the {market} space. 

You are responsible for generating consistent, clear, and compelling messaging based on user requests. 

You must be well versed in the market, business, and technical landscape of {company} to be effective in this role.
```

- {role}: the specific job function you want Claude to think like (PMM, Founder, etc.)
- {company}: use your company name so messaging comes from the right first-person 
- {stage}: the stage of company (emerging, growing, established)
- {type}: the type of company (B2B, B2C, E-Commerce, Services)
- {market}: your top-level market category (cybersecurity, developer tools, financial services, etc.)

## FAQ

**Why did you build this?**
I have to use Gemini at work. It's... messy. This is a lot more structured, a lot more focused, and a lot more fun to build.

**Isn't this overkill?**
Yes, probably for most. But when your company has multiple products serving multiple audiences across multiple segments, your regional teams are out there running wild, and your global sales reps are running even wilder, messaging gets real squirrely, real fast.

**Is Claude Code the right tool for this?**
No, probably not. But it has potential to get you into a messaging flow state that no other tool has been able to accomplish (yet).

## Contributing
I primarily encourage you to take this as-is and make it yours. But I do welcome PRs for the Messaging Blocks, Skills, Commands, and Agents. 

## History

Version 0.2 (2026-02-06) - system bootstrap
Version 0.1 (2026-01-16) - initial drop

## Credits
Ivan Dwyer (@fortyfivan)

## License
The MIT License (MIT)

Copyright (c) 2015 Chris Kibble

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.