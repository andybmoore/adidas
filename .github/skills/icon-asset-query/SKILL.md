---
name: icon-asset-query
description: "Find and analyze icon and flag assets in this repository. Use when users ask to locate files, compare naming patterns, find missing variants (rounded/square), inventory assets, or prepare query-ready summaries. Keywords: icons, flags, category, channel, division, naming, duplicates, coverage."
argument-hint: "task + scope, for example: find missing square variants in Flags"
user-invocable: true
---

# Icon Asset Query Skill

## When to Use
- A chat request asks where icon or flag files live.
- A user wants naming consistency checks across folders.
- A user asks for coverage checks (for example, rounded vs square flags).
- A user needs a quick inventory summary before making changes.

## Repository Scope
Primary folders in this repository:
- `Category Icons/`
- `Channels Icons/`
- `Division/`
- `Flags/Rounded/`
- `Flags/Square/`

## Procedure
1. Confirm the requested scope (single folder or all asset folders).
2. Gather files with fast search tools and summarize counts.
3. Normalize names for comparison (case-insensitive, extension-stripped).
4. Report findings:
   - Missing counterparts (rounded without square, and vice versa)
   - Possible duplicates by normalized name
   - Naming anomalies (spacing, separators, or inconsistent tokens)
5. If requested, propose a safe rename or move plan before editing files.

## Response Format
Use this compact output format for query responses:
1. Scope scanned
2. File counts by folder
3. Findings (missing variants, duplicates, naming anomalies)
4. Suggested next action

## Guardrails
- Do not rename or move files unless explicitly requested.
- Preserve existing folder structure unless user asks for reorganization.
- For potentially destructive changes, show a preview list first.
