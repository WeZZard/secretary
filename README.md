# WeZZard Skills

Personal Agent Skills for WeZZard, packaged as an [Agent Skills](https://agentskills.io/specification)
package installable via [npx skills](https://github.com/vercel-labs/skills).

## Skills

### Model-Invoked Skills

The agent loads these skills on its own when the task matches the description.

#### be-creative

Create a distinctive design direction using a random string as private inspiration. Use when designing visual or audio artifacts, such as interfaces, websites, graphics, videos, sound effects, and music, or when refining their style and elements.

Guides design through shell-generated randomness, interpretation of inspiring patterns, and polished execution without revealing the string in the result. Loads one reference per design dimension that the artifact has: visual, time, sound, and behavior, plus an audiovisual reference that joins visuals and sound.

#### bridge-on-x

Write a post. Use when bringing a subject from one community into another so newcomers read it through and care, for example introducing a developer project to designers or investors. Not for amplifying, reposting or announcing.

Carries a subject from one community into another with a hook, a plain how-it-works and an emotional push.

#### documentation

Write documents. Use when documenting.

Guides document authoring through `communicate` and its communication consistency rules, with established terminology and Mermaid diagrams where they improve comprehension.

#### explore

Explore requirements. Use when starting a design discussion.

Clarifies goals, intents, constraints, boundaries, and limitations from a top-down perspective. Settles each question from model knowledge, the internet, an experiment, or the user, in that order, and labels every inferred requirement with its source.

#### get-mood-on-x

Use before writing anything for an X account, and whenever that read may have changed: get a fresh read on who the author is, whom the author speaks for, and who the audience is right now, then hand a short brief to the writing skill, such as bridge-on-x.

Each run fetches new followers, bios and original posts on X, adds them to a local SQLite file, and reads the whole file before writing an audience brief of at most 120 words.

#### presentation

Present complex questions or work progress. Use when explaining a decision, plan, or result so the user can act on it.

Focuses on concerns, consequences, and recommended actions, asks questions with the dedicated question tool when one is available, switches to an illustrated HTML document when text alone would be tedious or ambiguous, and communicates through `communicate`.

#### repo-risk-audit

Audit an open-source project for risk. Use when deciding whether a GitHub project is safe to install, run, or give credentials to.

Launches separate subagents for provenance, issue verification, code audit, and supply chain audit on one pinned commit. Treats issue text and project claims as claims to verify, runs security tools such as Semgrep, Gitleaks, OSV-Scanner, and OpenSSF Scorecard, and delivers one verdict. Written with the key words of RFC 2119.

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

Guides top-down communication in plain language with established terminology.

Keeps communication consistent across conversations through `references/communication-consistency.md`: shows a visual glossary when the user may not recognize the parts of an artifact by name, pairs every identifier with a human-readable short name, reuses the project's existing identifiers, and fixes one named formula per measured quantity for the whole session.

#### experiment

Run a blind experiment. Use when settling a question that only trying can answer.

Produces 2–4 genuinely different candidates against a single criterion, blinds them behind letter labels, has them judged in a fixed verdict template, and leaves the ruling to the user. Uses external producers and judges when the dispatch plugin is installed.

## Installation

```bash
# Install the skills globally to Pi
npx skills add WeZZard/secretary -g -a pi \
  --skill be-creative --skill bridge-on-x --skill documentation --skill explore --skill get-mood-on-x --skill presentation --skill repo-risk-audit --skill troubleshoot \
  --skill code-review --skill communicate --skill experiment

# Verify with:
npx skills list -g

# Update after a change in this repo:
npx skills update be-creative bridge-on-x documentation explore get-mood-on-x presentation repo-risk-audit troubleshoot \
  code-review communicate experiment
```

> Note: `npx skills` installs to Pi via **copy** mode because only one agent is
targeted (the canonical+symlink model applies to multi-agent installs). The
installed skills are still fully managed by `npx skills` and tracked in
`~/.agents/.skill-lock.json`.

## Package Structure

Each skill is a directory containing a `SKILL.md` file with YAML frontmatter:

```
skills/
├── be-creative/
│   ├── SKILL.md
│   └── references/
│       ├── audiovisual.md
│       ├── behavior.md
│       ├── sound.md
│       ├── time.md
│       └── visual.md
├── bridge-on-x/
│   └── SKILL.md
├── code-review/
│   └── SKILL.md
├── communicate/
│   ├── SKILL.md
│   └── references/
│       └── communication-consistency.md
├── documentation/
│   └── SKILL.md
├── experiment/
│   └── SKILL.md
├── explore/
│   └── SKILL.md
├── get-mood-on-x/
│   └── SKILL.md
├── presentation/
│   └── SKILL.md
├── repo-risk-audit/
│   └── SKILL.md
└── troubleshoot/
    └── SKILL.md
```

## License

MIT — see [LICENSE](LICENSE).
