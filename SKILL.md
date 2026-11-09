---
name: project-standards-generator
description: Create or update a project-specific coding standards skill by examining the current repository and consulting official documentation. Use when the user wants to generate, maintain, or revise a project's development conventions as a reusable skill, including a focused update to an existing standards skill.
---

# Project Standards Generator

Create and maintain a project-specific standards skill grounded in the project's actual practices and relevant official documentation.

## Determine scope and destination

- Identify the repository and requested scope. For a multi-application repository, respect the scope the user specified; ask when module boundaries or intended scope are unclear.
- For an update, locate the existing standards skill and keep its location. Inspect its structure and affected rules before editing. A focused request needs only a focused investigation; expand it when evidence or conflicts require it.
- For a new skill, use the project's existing skills directory. If none exists, ask whether to use `.claude/skills` or `.agents/skills`. If both exist and neither contains the target skill, ask which to use. Honor an explicitly specified destination.
- Name the project skill `project-coding-standards` unless the user chooses another name.

## Gather evidence

- Inspect relevant project instructions, existing documentation, dependency and build configuration, directory layout, and representative implementation code. Expand the sample when conventions differ or evidence is insufficient. Follow repository instructions for code discovery.
- Record a project convention when project documentation or the user explicitly establishes it, or multiple code examples support it. A single example is a lead, not proof of a general convention.
- Consult official documentation for the languages, frameworks, and tools involved, preferably matching the project's dependency versions. Do not use community discussions as sources. Cite relevant official pages and project paths where they directly support a rule.
- Distinguish observed project conventions from official recommendations. Do not invent project practices. If official documentation or its applicable version cannot be verified, use confirmed project evidence and report the limitation in the conversation; do not add uncertainty markers to the generated skill.
- When existing practice differs from an official recommendation, describe the difference in the conversation and preserve the project convention. Flag security concerns or apparent errors rather than presenting them as standards without discussion.

## Design and approval

- Cover only relevant, useful topics supported by evidence, such as structure, language, framework, interfaces, testing, and build practices. Do not create empty sections for unused technologies.
- Organize the generated skill for progressive disclosure. Keep `SKILL.md` as a concise entry point that routes to focused reference files by module or concern. Each reference covers a coherent subset, so an agent reads only the rules needed for its task. Adapt the layout to the project rather than copying a fixed template.
- For updates, preserve unrelated and manually maintained rules. If a new requirement conflicts with an existing rule, show the conflict and proposed replacement for confirmation.
- Before creating or updating any skill files, show the user the intended file structure and a brief description of each affected file's contents. Wait for explicit confirmation before writing. For focused updates, show the affected files and proposed changes; do not require a full repository rescan.

## Write and verify

- After confirmation, write concise, actionable instructions and retain only relevant source references. Keep official recommendations distinguishable from project conventions.
- Validate skill frontmatter, name, file structure, internal links, and consistency between affected rules. Use an available skill validator where practical. Project builds and tests are not implied by documentation-only edits.
- Report changed files, validation results, material conflicts, and documentation or versions that could not be verified in the conversation.
