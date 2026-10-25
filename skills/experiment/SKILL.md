---
name: experiment
description: "Use when settling a question only trying can answer."
disable-model-invocation: true
---

# Experiment

## Goal

Conduct experiments to answer questions with the protocol and the verdict contract.

## Protocol

1. **Frame.** Name the experiment (kebab-case) and write the single criterion the candidates compete on. A candidate set without a criterion is a preference poll, not an experiment.
2. **Produce.** Produce 2–4 candidates of the same content into `${TMPDIR:-/tmp}/agent-experiments/<name>/`, each committed to a genuinely different approach (structure, register, length — name each approach before writing). With the dispatch plugin installed, widen the set with external producers — one router brief per producer (`AGENTS: <agent>` pins which agent produces the candidate; the router brief's `## Response` section asks for the candidate text verbatim) — and always produce at least one candidate yourself.
3. **Blind.** Copy the candidates to letter labels (`A.md`, `B.md`, …) in shuffled order (use `$RANDOM`), stripping every provenance hint from the content. Write the letter-to-producer allocation key to `allocation-key.txt`; never show it to a judge and never quote it before the ruling.
4. **Judge.** With the dispatch plugin installed, send each judge the letter-labeled candidates and the criterion — one router brief per judge (`TAGS: auditing`, `AGENTS: <agent>` to pin it), 2–3 external judges in parallel, each router brief's `## Response` section carrying the verdict contract below as **MUST:** / **MUST NOT:** lists — and save each returned verdict verbatim to `verdicts/<judge>.md` in the experiment directory. Without the dispatch plugin, judge the letter-labeled candidates yourself against the criterion alone: read them in letter order, one fresh reading per candidate, and write each verdict to `verdicts/` in the template below before reading on — you produced these candidates, so the verdicts share your biases; say so when you present them.
5. **Rule.** Present a compiled comparison to the user: each candidate's path, the rankings across judges, and each verdict's file path so the user can check the reasoning — never quote a verdict partially in a way that reshapes it. The user rules. Reveal the allocation key only after the ruling.
6. **Conclude.** Report the ruling as the experiment's outcome to the task that requested it. Leave the experiment directory in place — candidates, the allocation key, and verdicts are the experiment's evidence trail; never reuse them as design artifacts.

## The Verdict Contract

**MUST:**

1. You **MUST** write every verdict — external or your own — in the template below.
2. You **MUST** rank against the stated criterion alone.
3. You **MUST** justify the ranking in two sentences.

**MUST NOT:**

1. You **MUST NOT** use all-caps section titles or labels in the template.
2. You **MUST NOT** let a router brief or a verdict carry any provenance hint.

Required verdict template:

```markdown
## Ranking
<letters, best to worst>

## Justification
<two sentences against the criterion>
```

## Isolation

- Producers and judges **MUST** run read-only.
- The experiment **MUST** run in a detached git worktree when the experiment requires writing into a repository. The diff collected there is the evidence. Merging stays an explicit step in the main agent

<GIT_WORKTREE_COMMAND_EXAMPLES>
Create: `git -C <repo-dir> worktree add --detach <worktree-path>`.
Cleans up: `git -C <repo-dir> worktree remove <worktree-path>`.
</GIT_WORKTREE_COMMAND_EXAMPLES>
