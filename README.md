# WeZZard Skills

Personal Agent Skills for WeZZard, packaged as an [Agent Skills](https://agentskills.io/specification)
package installable via [npx skills](https://github.com/vercel-labs/skills).

## Skills

### documentation

Write documents. Use when producing, editing, or reviewing any document, doc comment, README, or written deliverable.

Guides document authoring to industry-standard format in simple and plain language.

### presentation

Present any contents in the conversation other than small talks. Use when explaining a decision, plan, or result so the user can act on it.

Guides presenting ideas in simple and plain language, focused on concerns, consequences, and recommended actions.

## Installation

```bash
# Install both skills globally to Pi
npx skills add WeZZard/secretary -g -a pi --skill documentation --skill presentation

# Or install globally with symlink mode (default). Verify with:
npx skills list -g
```

## Package Structure

Each skill is a directory containing a `SKILL.md` file with YAML frontmatter:

```
skills/
├── documentation/
│   └── SKILL.md
└── presentation/
    └── SKILL.md
```

## License

MIT — see [LICENSE](LICENSE).
