# Workflow Pattern

All Messaging House component skills follow this 6-step research-first workflow.

## Standard Workflow

```
1. LOAD CONTEXT
   → Read prior /messaging/ components
   → Scan /research/ directory for local content
   → Extract relevant facts and context

2. RESEARCH
   → Summarize what's available locally
   → WebSearch only for gaps
   → Extract key data points

3. PRESENT FINDINGS
   → Show discovered information
   → Note what came from local vs. search
   → Highlight gaps needing input

4. CONFIRM & REFINE
   → User validates findings
   → Fills gaps with options
   → 4-5 questions maximum

5. GENERATE
   → Create messaging blocks
   → Follow output format exactly
   → Write to /messaging/{component}.md

6. VALIDATE
   → Self-check against criteria
   → Verify completeness
```

## Research Priority Order

Skills check content sources in this order:

1. **Local `/research/` directory** - User-provided documents
2. **Prior `/messaging/` components** - Completed messaging blocks
3. **WebSearch** - Only for information not found above

## Scan & Summarize Pattern

When checking `/research/`:

```
1. Glob /research/*.* to list files
2. Read relevant files
3. Present summary:

   LOCAL RESEARCH AVAILABLE

   Found {N} files in /research/:
   - {file1}: Contains {summary}
   - {file2}: Contains {summary}

   Relevant to this skill:
   - {what I'll extract}

   Still need to search for:
   - {gaps}
```

## Presentation Format

Use consistent formatting for findings and questions:

```
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
SECTION HEADER
Content here
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

## Question Format

```
1. Question text?

   Context: [why this matters]

   Options:
   - [ ] Option A (Recommended)
   - [ ] Option B
   - [ ] Other: [describe]
```

## Validation Pattern

Each skill defines criteria. Check:
- [ ] Research quality (sources checked, gaps identified)
- [ ] Content quality (block-specific criteria)
- [ ] Format compliance (exact structure followed)
