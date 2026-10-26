# WeZZard Skills

Personal Agent Skills for WeZZard, packaged as an [Agent Skills](https://agentskills.io/specification)
package installable via [npx skills](https://github.com/vercel-labs/skills).

## Skills

### Model-Invoked Skills

The agent loads these skills on its own when the task matches the description.

#### documentation

Write documents. Use when producing, editing, or reviewing any document, doc comment, README, or written deliverable.

Guides document authoring to industry-standard format in simple and plain language, with Mermaid diagrams where they improve comprehension and consistent terminology through `communication-consistency`.

#### education

Produce learning material. Use when teaching the user a topic, paper, system, or result so they can understand and explain it afterwards.

States a learning goal first, defines terms in a glossary, and teaches concepts one at a time with an example, an illustration, and a self-check. Asks questions with the dedicated question tool when one is available, and communicates through `communicate` and `communication-consistency`.

#### explore

Explore requirements. Use when starting a design discussion.

Clarifies goals, intents, constraints, boundaries, and limitations from a top-down perspective. Settles each question from model knowledge, the internet, an experiment, or the user, in that order, and labels every inferred requirement with its source.

#### presentation

Present complex questions or work progress. Use when explaining a decision, plan, or result so the user can act on it.

Focuses on concerns, consequences, and recommended actions, asks questions with the dedicated question tool when one is available, and communicates through `communicate`.

#### troubleshoot

Troubleshoot a reported issue end to end. Use when a bug or defect is reported and needs reproduction, root cause analysis, an architectural fix, and a documented plan.

Drives troubleshooting with an end-to-end reproducer, lands an architectural fix with updated documents, and records a plan in the `.plans` directory citing the document changes.

### Manually Invoked Skills

These skills set `disable-model-invocation: true`. They load only when the user or the invoking prompt names them, for example `/code-review`.

#### code-review

Review a change set unattended. Use when reviewing a change in a CI pipeline before merge.

Reports only demonstrated findings, graded as blocking or advisory, checked against the project's recorded decisions and design docs, and written as a JSON report the pipeline can gate on.

#### communicate

Communicate with the user. Use for any message to the user.

Guides top-down communication in plain language with established terminology, and switches to an illustrated HTML document when text alone would be tedious or ambiguous.

#### communication-consistency

Keep communication consistent across conversations. Use when communicating with the user.

Pairs every identifier with a human-readable short name, reuses the project's existing identifiers, and fixes one named formula per measured quantity for the whole session.

#### experiment

Run a blind experiment. Use when settling a question that only trying can answer.

Produces 2–4 genuinely different candidates against a single criterion, blinds them behind letter labels, has them judged in a fixed verdict template, and leaves the ruling to the user. Uses external producers and judges when the dispatch plugin is installed.

#### visual-design

Create a distinctive visual direction using a random string as private inspiration. Use when designing interfaces, websites, graphics, or other visual artifacts, or refining their color scheme, layout, and typography.

Guides design through shell-generated randomness, interpretation of inspiring patterns, and polished execution without revealing the string in the result.

## Installation

```bash
# Install the skills globally to Pi
npx skills add WeZZard/secretary -g -a pi \
  --skill documentation --skill education --skill explore --skill presentation --skill troubleshoot \
  --skill code-review --skill communicate --skill communication-consistency \
  --skill experiment --skill visual-design

# Verify with:
npx skills list -g

# Update after a change in this repo:
npx skills update documentation education explore presentation troubleshoot \
  code-review communicate communication-consistency experiment visual-design
```

> Note: `npx skills` installs to Pi via **copy** mode because only one agent is
targeted (the canonical+symlink model applies to multi-agent installs). The
installed skills are still fully managed by `npx skills` and tracked in
`~/.agents/.skill-lock.json`.

## Package Structure

Each skill is a directory containing a `SKILL.md` file with YAML frontmatter:

```
skills/
├── code-review/
│   └── SKILL.md
├── communicate/
│   └── SKILL.md
├── communication-consistency/
│   └── SKILL.md
├── documentation/
│   └── SKILL.md
├── education/
│   └── SKILL.md
├── experiment/
│   └── SKILL.md
├── explore/
│   └── SKILL.md
├── presentation/
│   └── SKILL.md
├── troubleshoot/
│   └── SKILL.md
└── visual-design/
    └── SKILL.md
```

## License

MIT — see [LICENSE](LICENSE).
