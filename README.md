# Obsidian Plugin Skills for Claude Code

Claude Code skills for popular Obsidian plugins. These reference documents help Claude generate accurate plugin-specific syntax.

## What are Claude Code Skills?

[Skills](https://docs.anthropic.com/en/docs/claude-code/skills) are markdown files that Claude automatically loads when relevant keywords appear in your requests. When you mention "Dataview query" or "Templater template", Claude references these skills to generate correct syntax.

## Available Skills

| Skill | Plugin | Upstream PR |
|-------|--------|-------------|
| [Dataview](skills/dataview/SKILL.md) | [obsidian-dataview](https://github.com/blacksmithgu/obsidian-dataview) | [#2651](https://github.com/blacksmithgu/obsidian-dataview/pull/2651) |
| [Templater](skills/templater/SKILL.md) | [Templater](https://github.com/SilentVoid13/Templater) | [#1682](https://github.com/SilentVoid13/Templater/pull/1682) |
| [Tasks](skills/tasks/SKILL.md) | [obsidian-tasks](https://github.com/obsidian-tasks-group/obsidian-tasks) | [#3732](https://github.com/obsidian-tasks-group/obsidian-tasks/pull/3732) |

## Installation

Copy the `skills` folder to your vault's `.claude` directory:

```
your-vault/
├── .claude/
│   └── skills/
│       ├── dataview/SKILL.md
│       ├── templater/SKILL.md
│       └── tasks/SKILL.md
└── ... your notes ...
```

Or clone this repo and symlink:

```bash
git clone https://github.com/sunnyhasija/obsidian-plugin-skills.git
ln -s /path/to/obsidian-plugin-skills/skills /path/to/your-vault/.claude/skills
```

## Skill Coverage

### Dataview
- DQL query types (LIST, TABLE, TASK, CALENDAR)
- FROM/WHERE/SORT/GROUP BY/FLATTEN clauses
- Inline fields and implicit fields
- All functions (string, numeric, date, array)
- DataviewJS API

### Templater
- Template syntax (`<% %>` vs `<%* %>`)
- All tp.* modules (date, file, system, web, config, frontmatter, hooks)
- Moment.js date formatting
- Complete template examples

### Tasks
- Task syntax (emojis and text formats)
- All date types and priorities
- Recurrence patterns
- Query filters, sorts, groups
- Custom statuses

## Related Projects

- [kepano/obsidian-skills](https://github.com/kepano/obsidian-skills) - Core Obsidian syntax (Markdown, Canvas, Bases)

## License

MIT
