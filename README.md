# Project Standards Generator

[中文](README.zh-CN.md)

Generate and maintain a project-specific coding standards skill from repository evidence and official documentation. The generated skill organizes conventions by topic and loads relevant guidance on demand.

## What it does

- Inspects the project's structure, configuration, documentation, and representative code.
- Consults official documentation, preferably matching the project's dependency versions.
- Separates observed project conventions from official recommendations.
- Organizes the resulting skill into a concise `SKILL.md` and focused reference files.
- Updates existing standards without overwriting unrelated rules.
- Shows the proposed file structure and content before writing, then validates the result.

## Use

Install this repository as a skill in your agent's skills directory, following your agent's installation instructions. Then ask your agent, for example:

```text
Use project-standards-generator to create a coding standards skill for this project.
```

To update an existing project skill:

```text
Use project-standards-generator to update the project coding standards: <describe the rule>.
```

The generator asks for confirmation before creating or updating skill files. When official documentation cannot be verified, it reports the limitation in the conversation.
