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

# Verify with:
npx skills list -g

# Update after a change in this repo:
npx skills update documentation presentation
```

> Note: `npx skills` installs to Pi via **copy** mode because only one agent is
targeted (the canonical+symlink model applies to multi-agent installs). The
installed skills are still fully managed by `npx skills` and tracked in
`~/.agents/.skill-lock.json`.

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
