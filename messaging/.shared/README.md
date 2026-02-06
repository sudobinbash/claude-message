# Shared Templates

This directory contains reusable patterns and templates for Messaging House skills.

## Contents

| File | Purpose |
|------|---------|
| workflow-pattern.md | Standard 6-step research-first workflow |
| profile-templates.md | Templates for element profiles (personas, products, etc.) |

## How Skills Use These

Skills reference these patterns but remain self-contained. The shared templates provide:
- Consistent workflow structure across all component builders
- Standardized profile formats for element types
- Common presentation formats for findings and confirmations

## Workflow Pattern

All Messaging House skills follow a consistent 6-step pattern:

1. **Load Context** - Read prior components and `/research/` directory
2. **Research** - WebSearch for gaps not covered by local content
3. **Present Findings** - Show what was discovered
4. **Confirm & Refine** - User validates and adds input
5. **Generate** - Create messaging blocks
6. **Validate** - Self-check against quality criteria

See `workflow-pattern.md` for full details.

## Profile Templates

Element profiles (personas, products, competitors, etc.) use standardized templates.
See `profile-templates.md` for all template formats.
