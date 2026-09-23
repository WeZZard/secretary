---
name: experiment
description: "Use when settling a question only trying can answer."
disable-model-invocation: true
---

# Experiment — Settle by Evidence

**Announce at start:** "I'm running an experiment to settle this by evidence."

## When

A question only new experience can answer — nothing recorded holds it yet: "does the shorter opening actually read better?", "does this voice survive the blog medium?". If it is a judgment, the user rules directly — explore's Ask step puts the judgment to them prepared; run the experiment when they want that ruling informed by blind evidence. If the web already holds the answer, research settles it — no experiment. An experiment runs only after research comes back empty.

## External producers

When the dispatch plugin is installed, its `use-external-agents` skill reaches external agents in the producer and judge roles — invoke that skill before composing any router brief; it defines the router and the router brief contract. Without the dispatch plugin, you produce and judge yourself, and the protocol below says how at each step.

## Protocol

1. **Frame.** Name the experiment (kebab-case) and write the single criterion the candidates compete on. A candidate set without a criterion is a preference poll, not an experiment.
2. **Produce.** Produce 2–4 candidates of the same content into `${TMPDIR:-/tmp}/agent-experiments/<name>/`, each committed to a genuinely different approach (structure, register, length — name each approach before writing). With the dispatch plugin installed, widen the set with external producers — one router brief per producer (`AGENTS: <agent>` pins which agent produces the candidate; the router brief's `## Response` section asks for the candidate text verbatim) — and always produce at least one candidate yourself.
3. **Blind.** Copy the candidates to letter labels (`A.md`, `B.md`, …) in shuffled order (use `$RANDOM`), stripping every provenance hint from the content. Write the letter-to-producer allocation key to `allocation-key.txt`; never show it to a judge and never quote it before the ruling.
4. **Judge.** With the dispatch plugin installed, send each judge the letter-labeled candidates and the criterion — one router brief per judge (`TAGS: auditing`, `AGENTS: <agent>` to pin it), 2–3 external judges in parallel, each router brief's `## Response` section carrying the verdict contract below as **MUST:** / **MUST NOT:** lists — and save each returned verdict verbatim to `verdicts/<judge>.md` in the experiment directory. Without the dispatch plugin, judge the letter-labeled candidates yourself against the criterion alone: read them in letter order, one fresh reading per candidate, and write each verdict to `verdicts/` in the template below before reading on — you produced these candidates, so the verdicts share your biases; say so when you present them.
5. **Rule.** Present a compiled comparison to the user: each candidate's path, the rankings across judges, and each verdict's file path so the user can check the reasoning — never quote a verdict partially in a way that reshapes it. The user rules. Reveal the allocation key only after the ruling.
6. **Conclude.** Report the ruling as the experiment's outcome to the task that requested it. Leave the experiment directory in place — candidates, the allocation key, and verdicts are the experiment's evidence trail; never reuse them as design artifacts.

## The verdict contract

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

Producers and judges run read-only. When a future experiment requires writing into a repository, work in a detached git worktree, never the repository itself: `git -C <repo-dir> worktree add --detach <worktree-path>` creates it, the diff collected there is the evidence, merging stays an explicit step in the main agent, and `git -C <repo-dir> worktree remove <worktree-path>` cleans up. With the dispatch plugin installed, its `use-external-agents` skill carries the worktree tooling and the write-isolation rules for external agents.
