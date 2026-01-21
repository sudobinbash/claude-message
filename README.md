██████╗██╗      █████╗ ██╗   ██╗██████╗ ███████╗
██╔════╝██║     ██╔══██╗██║   ██║██╔══██╗██╔════╝
██║     ██║     ███████║██║   ██║██║  ██║█████╗  
██║     ██║     ██╔══██║██║   ██║██║  ██║██╔══╝  
╚██████╗███████╗██║  ██║╚██████╔╝██████╔╝███████╗
 ╚═════╝╚══════╝╚═╝  ╚═╝ ╚═════╝ ╚═════╝ ╚══════╝

███╗   ███╗███████╗███████╗███████╗ █████╗  ██████╗ ███████╗
████╗ ████║██╔════╝██╔════╝██╔════╝██╔══██╗██╔════╝ ██╔════╝
██╔████╔██║█████╗  ███████╗███████╗███████║██║  ███╗█████╗  
██║╚██╔╝██║██╔══╝  ╚════██║╚════██║██╔══██║██║   ██║██╔══╝  
██║ ╚═╝ ██║███████╗███████║███████║██║  ██║╚██████╔╝███████╗
╚═╝     ╚═╝╚══════╝╚══════╝╚══════╝╚═╝  ╚═╝ ╚═════╝ ╚══════╝

Claude Message is an opinionated, yet customizable messaging framework built around the Claude Code harness. It acts as the positioning and messaging context engine for Claude Code to generate content assets – ensuring the copy always strikes a chord and is uniquely yours.

This is meant for Product Marketers, Founders, and anyone who cares about messaging quality and taste. It's built primarily for B2B companies, but the principles may apply to others.

A basic understanding of how to use Claude Code, and how its harness works is required.

The tl;dr - fork it, tune to your market, write to your message, generate dope content. 

*I said who's house? Your house!*

## How it Works

The contents of this repository form the foundational architecture for your own custom messaging system. Your business is dynamic, your messaging must be too.

### Messaging House

The Messaging House is a structured model of your positioning and messaging. It covers every aspect of your market space, product offering, and go-to-market engine. The core components include:

- Purpose: your vision and mission
- Profile: your company foundation
- Position: your market space
- Proposition: your unique value
- Pitch: your differentiated narrative
- People: your target audience
- Portfolio: your market offering
- Proof: your evidence of value
- Plays: your go-to-market
- Preferences: your brand voice

Within the components, there are specific elements that may contain multiple profiles. To ensure relevancy, carve out dedicated profiles for:

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

Edit the markdown files in the root `messaging` directory to design your Messaging House. There is one markdown file for each element, which includes a number of Messaging Blocks. Each block is complemented with helpful instructions, tips, and format guidance. These are just suggestions, make it yours!

Review the contents of each Skill in the `.claude/skills/` directory. There is a working markdown file for each included Skill, but you may want to customize the instructions and output format template, and/or provide your own examples for additional reference.

Review the contents of each Command in the `.claude/commands/` directory. There is a working markdown file for each included Command, but you may want to provide your own instructions.

Once you are comfortable with the Messaging House and Messaging Skills contents, edit the main `CLAUDE.md` file to tune your writing profile and exactly how Claude Code interacts with the system. 

It is a lot of work to customize this system to your company messaging. Hopefully a lot of this already exists in some form or fashion, so it's a matter of organization and polish. If this doesn't exist, it's worth the exercise to get this into a good place regardless of your use of this repository. 

## Your Writing Profile

You can't change the main Claude Code system prompt, but you can provide a profile to guide its writing style. It's recommended to provide Claude Code with a more personal writing profile, rather than some generic, "you are a writing agent."

The default format provided in the sample `CLAUDE.md` file follows this structure:

```
You are a {role} at {company}. {company} is a(n) {stage} {type} company in the {market} space. You are responsible for generating consistent, clear, and compelling messaging based on user requests. You must be well versed in the market, business, and technical landscape of {company} to be effective in this role.
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

Version 0.1 (2026-01-16) - initial drop

## Credits
Ivan Dwyer (@fortyfivan)

## License
The MIT License (MIT)

Copyright (c) 2015 Chris Kibble

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.