# Claude Code Skills

A collection of custom skills for [Claude Code](https://claude.ai/code).

## Skills

| Skill | Description |
|-------|-------------|
| [git-clean-local](.claude/skills/git-clean-local/SKILL.md) | Cleans up local workspace after merging a git feature branch from an open PR |

## Usage

Clone this repository, then point Claude Code at it using the `--add-dir` flag:

```bash
git clone https://github.com/drakestr/claude-code-skills.git
claude --add-dir /path/to/claude-code-skills
```

Skills in `.claude/skills/` are automatically discovered and available immediately. You can invoke any skill by name during a conversation.

> [!NOTE]
> The recommended approach is to add this as an additional directory via `settings.json`:
>
> ```json
> {
>   "permissions": {
>     "additionalDirectories": [
>       "/path/to/claude-code-skills"
>     ]
>   }
> }
> ```
>
> However, this is currently broken due to a [known bug](https://github.com/anthropics/claude-code/issues/30064). Use the `--add-dir` flag as a workaround until the issue is resolved.

## Structure

```
.claude/skills/
└── <skill-name>/
    └── SKILL.md
```

Each skill is a `SKILL.md` file with frontmatter (`name`, `description`) and instructions that Claude Code follows when the skill is invoked.
