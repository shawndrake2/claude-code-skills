# Claude Code Skills

A collection of custom skills for [Claude Code](https://claude.ai/code).

## Skills

| Skill | Description |
|-------|-------------|
| [git-clean-local](.claude/skills/git-clean-local/SKILL.md) | Cleans up local workspace after merging a git feature branch from an open PR |

## Installation

Add this repository as an additional directory in your Claude Code `settings.json`:

```json
{
  "additionalDirectories": [
    "/path/to/claude-code-skills"
  ]
}
```

Skills in `.claude/skills/` are automatically discovered and available immediately.

## Structure

```
.claude/skills/
└── <skill-name>/
    └── SKILL.md
```

Each skill is a `SKILL.md` file with frontmatter (`name`, `description`) and instructions that Claude Code follows when the skill is invoked.
