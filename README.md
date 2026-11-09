# Project Standards Generator

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

---

# 项目规范生成器

根据项目代码和官方文档，生成并维护项目专属的开发规范 skill。生成的规范按主题组织，按需加载相关内容。

## 功能

- 检查项目结构、配置、文档和代表性代码。
- 查阅官方文档，优先匹配项目依赖版本。
- 区分项目现有约定与官方建议。
- 将规范组织为精简的 `SKILL.md` 和按主题拆分的参考文件。
- 更新已有规范时保留无关规则。
- 写入前展示拟定的文件结构和内容，完成后验证结果。

## 使用

按照所用 agent 的安装说明，将本仓库安装到 skills 目录。然后向 agent 发出请求，例如：

```text
使用 project-standards-generator 为当前项目创建开发规范 skill。
```

更新现有项目规范：

```text
使用 project-standards-generator 更新项目开发规范：<描述要添加或修改的规则>。
```

生成器会在创建或更新文件前请求确认。无法核实官方文档时，会在对话中说明。
