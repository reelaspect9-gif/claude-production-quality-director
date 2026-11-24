# Production Quality Director

A standalone Claude Code subagent for independent, evidence-based production review. It checks briefs, consequential decisions, artifacts, and delivery gates, then returns **PASS**, **REWORK**, or **BLOCKED** with concrete findings.

Repository: https://github.com/reelaspect9-gif/claude-production-quality-director

Agent definition: [production-quality-director.md](.claude/agents/production-quality-director.md)

This is a prompt-based reviewer. It is **not an automatic tool interceptor, background monitor, permission system, or guarantee of perfection**. The lead must provide artifacts, request reviews, maintain the action ledger, and enforce the resulting gates. The definition has not been live-tested in Claude Code.

## What it reviews

- Actionable briefs, supported facts, explicit requirements, and consequential decisions.
- Construction, blueprint/dimension evidence, geometry, materials, effective texture detail, and functional assets.
- Character/style consistency, physical contact, readable motion, camera work, and temporal stability.
- Contextual typography, edit continuity, actual audio evidence, and final encoded output.
- Editable delivery, dependencies, packaging, and the checks that were actually performed.

The reviewer distinguishes defects from optional taste. It does not secretly repair another worker's implementation or invent watched footage, heard audio, unavailable tools, or successful tests.

## Install in a project

1. Open the project that should use this reviewer.
2. Check for an existing `.claude/agents/production-quality-director.md`. Preserve customizations and compare definitions before an authorized replacement; do not overwrite existing work silently.
3. Copy the repository's `.claude/agents/production-quality-director.md` to the same relative path in your project. Create the directory if needed and authorized.
4. Keep the YAML frontmatter and exact `.md` extension intact. Save as UTF-8.
5. Start a fresh Claude Code session and verify discovery through the available agent list, including `/agents` where supported.

For user-level availability, the standard destination is `~/.claude/agents/production-quality-director.md` instead. On Windows, this normally resolves beneath `%USERPROFILE%\.claude\agents\`. Choose the intended scope and avoid maintaining conflicting copies unintentionally.

Official format and discovery documentation: https://code.claude.com/docs/en/sub-agents

## Fit it into the existing team

If your project already uses an AI Templates Prompt Engineer, keep that agent as the primary prompt-engineering role. The intended order is:

**Existing Prompt Engineer → supporting Prompt Architect → Quality Director brief review → implementation → Quality Director at required gates.**

This repository does not install, replace, or duplicate the Prompt Engineer or Prompt Architect. Use actual available workers and preserve the project's existing workflow.

## Delegate with real inputs

Example brief review:

> Use the production-quality-director subagent to review this production brief and action plan. Provide the current requirements, accepted references, decisions, and expected deliverables. Return PASS, REWORK, or BLOCKED with evidence and precise correction targets.

Example artifact review:

> Ask production-quality-director to review this candidate sequence. Give it the actual media, source version, inspected frame range, manifests, and acceptance criteria. Keep the review independent; return findings rather than editing implementation files.

Do not assume `/production-quality-director` is a slash command. Invoke the subagent through natural-language delegation or the mechanisms supported by your Claude Code version.

## Interpret the result

- **PASS:** the stated scope satisfies its mandatory criteria with sufficient evidence.
- **REWORK:** demonstrated defects need correction and a defined recheck.
- **BLOCKED:** a necessary input or capability prevents a required conclusion; unaffected work can continue.

The definition does not install rendering, browsing, audio, or editing tools. Available capabilities determine which checks can actually run. Agent discovery alone does not establish that a production review has occurred.
