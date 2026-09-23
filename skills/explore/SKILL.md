---
name: explore
description: "Use when starting a design discussion."
disable-model-invocation: true
---

# Explore — Ask, Sort, Research, Experiment

**Announce at start:** "I'm using the explore skill."

## Goal

A design discussion where the model drives: the model raises the hard questions itself — purpose, alternatives, shortcuts — answers everything its own instruments can reach, and brings the user only what only the user can supply: their facts (deadlines, constraints, context) and their rulings (taste, priorities, risk). The discussion ends with decisions resting on evidence and rulings, never on assumptions. Every rule below serves this goal. A rule that stops serving it is a defect — report it to the user for repair in this document, never waive it at runtime: no step or rule may be skipped by appeal to the goal.

## Potential Step: Ask

**When to use:**

1. Aimed at yourself: a design-shaped idea enters the discussion; a solution is proposed whose purpose has not been stated; a decision nears with only one candidate on the table; new evidence contradicts the current understanding.
2. Aimed at the user: sorted user-specific questions have accumulated to fill one question call; one alone blocks a pending decision; or the pass is about to present with user-specific questions still open — none survives to the presentation unasked unless parked there by name.

**MUST:**

1. You **MUST** investigate what the user is ultimately trying to make happen: why it matters, who it serves, and what observable change would count as success — treating the stated request as an entry point, not a specification.
2. You **MUST** walk up the means–end hierarchy: purpose (why it matters), intent (what the user is trying to make happen), outcome (the observable change), approach (a class of interventions), solution (one concrete implementation) — better options become visible at higher levels.
3. You **MUST** generate alternatives that differ in mechanism, not in wording: reframe the problem at a different level, remove or reverse an assumption, change the audience, reorder or delete steps, move work between people and systems, borrow a pattern from another domain, reach the outcome without the requested artifact, or build nothing.
4. You **MUST** seek a shorter path — a shortcut that reaches the outcome with less work, cost, delay, or risk — with the sources already within reach, memory and this machine (the web-wide search is Research's gated exploratory search), and compare a found one against the original proposal on outcome, complexity, risk, and reversibility.
5. You **MUST** keep a short written summary of the current best guess — purpose, desired outcomes, affected people, constraints, open tensions — and revise it whenever an alternative, a finding, or a ruling moves it.
6. You **MUST** add every question this step raises to the discussion's open list — kept as visible text in the thread, never only in your head.
7. You **MUST** put to the user only questions Sort has marked user-specific, each in its shape: a private fact asked plainly; an intent or context question carrying your current best reading ("I take the goal to be X — correct me"); a judgment prepared — relevant facts settled where they already exist, tradeoffs laid out with fact separated from judgment, a recommendation carried with its reason.
8. You **MUST** ask one question call at a time — a call is one use of the question tool, or one direct question in conversation where none exists; a call may batch up to four independent, related forks — parallel questions carried in one call — each in its kind's shape.
9. You **MUST** state the settled ruling explicitly before the next question call, and carry it into the work at hand.
10. You **MUST** route a fact held by a third party — a teammate, a platform owner — or an environment only the user can grant through the user: ask who can answer it or how to reach it. A routing request is not a judgment question; it needs no recommended answer.
11. You **MUST**, when a judgment blocks a decision, ask regardless of pacing — or park the decision by recording it in the presentation as open, with what blocks it.

**MUST NOT:**

1. You **MUST NOT** confuse the requested artifact with the purpose behind it.
2. You **MUST NOT** present cosmetic variations of one mechanism as different alternatives.
3. You **MUST NOT** call an approach a shortcut when it moves hidden cost, risk, or effort onto another person.
4. You **MUST NOT** restate the request at a higher level of abstraction and present it as insight.
5. You **MUST NOT** keep interrogating once answers stop changing the decision — when the last two answers moved nothing, move on.
6. You **MUST NOT** present a judgment's outcome as an objective conclusion — when the user wants blind evidence, the Experiment step prepares it, and the user still rules.
7. You **MUST NOT** outsource the generation of alternatives to the user under the pretense of asking for clarification.
8. You **MUST NOT** let question pacing license assuming: roughly 4–6 question calls per pass is the comfortable rhythm, a guide and never a cap.
9. You **MUST NOT** offer a menu for a decision you can settle yourself.

## Potential Step: Sort

**When to use:**

1. The open list holds an unsorted question — always, before any work proceeds on that question. This is the one unconditional step in this skill, and the gate between Ask's two aims.

**MUST:**

1. You **MUST** classify each question once: a verifiable fact (evidence anyone can gather settles it), a private fact (only the user's own world holds it — a deadline, a constraint, what their team runs), or a judgment (the user's answer is the answer — taste, priorities, risk tolerance, what matters most).
2. You **MUST** mark private facts and judgments user-specific — the mark Ask's user aim consumes; a verifiable fact stays unmarked unless it is held by a third party or behind access only the user can grant, in which case it keeps its kind and is marked user-specific as a routing request: the user is asked for the route, never the answer.
3. You **MUST** sort by whether answering requires deciding: an answer the user could recite without deciding anything — a recorded fact, an observable state, an already-set policy — is a fact; an answer that requires deciding, here and now, is a judgment. When you cannot tell which, shape it as a judgment — over-preparing a fact is safe; under-preparing a judgment is not. This tie-break chooses the shape of a question already the user's; it never moves a question you can settle to the user.
4. You **MUST** decompose a compound question into its parts and route each on its own: a forecast, or a prediction about an unbuilt thing, is evidence parts plus a risk ruling — and a risk the user would plainly accept is recorded as a visible assumption in the presentation instead of asked.

**MUST NOT:**

1. You **MUST NOT** let any question reach the user unsorted.

## Potential Step: Research

**When to use:**

1. A sorted verifiable fact blocks a pending decision, or its answer would change which option wins.

**MUST:**

1. You **MUST** settle it through the source order — memory, this machine, the web — taking the cheapest source that can settle it; most research ends at memory or this machine without touching the web.
2. You **MUST** move to the next source when the source cannot settle the question, and skip a source only when it obviously cannot hold the answer — your unpublished design is not on the web — saying so when you skip.
3. You **MUST** keep the recalled facts the design leans on listed in the thread — in the research digest when one exists, otherwise in the pass's presentation; a fact is load-bearing when the design changes if it is wrong, and when unsure, it is.
4. You **MUST** verify each load-bearing recall against its source before the pass presents its recommendation — once, batched, only for the load-bearing survivors, never a research effort per question; recall stays the cheap path because the checks run at the end.
5. You **MUST** offer one exploratory search once the user's intent is settled — at most one per settled intent — and run it only on the user's go-ahead.

**MUST NOT:**

1. You **MUST NOT** answer from beliefs about the system under study within reach — this repository, an installed library, a running service — when observation can settle it, nor with code that restates beliefs: code that answers for the system under study runs against that system.

**Source 1 — memory.** Settle in-thread what the model already holds, when the fact is stable, pre-cutoff, and not about this machine, this repository, or this user — stating it plainly as recalled. Treat prices, defaults, versions, deprecations, and anything a release note could change as volatile, never stable. Stable, documented behavior of a widely known system beyond reach ("does Python's sort guarantee stability?") is ordinary memory, subject to the load-bearing list. Derivation counts as memory's strong form: for a question about a mathematical or algorithmic object, reason it out or write and run code that computes it, and show the work.

**Source 2 — this machine.** When the answer lives here — the repository, a running process, an installed tool — observe it: read the code, run the command, or run a small probe against the local system ("does this regex backtrack on our inputs?" is a one-line probe, not a research task). Observation settles what the system *does*; documentation research settles what it *promises*; a question that spans both splits.

**Source 3 — the web.** For answers recorded outside the session's reach, run grounded research, one researcher per question. Every researcher writes its full research brief to `${TMPDIR:-/tmp}/agent-explore/<topic>/<question>.md` (`<topic>`: the kebab-case name of the discussion's subject) — the research brief files are the evidence trail; the thread carries only the compiled digest. A research brief written before this pass began is history, not current evidence — re-validate before reusing it.

<!-- @port claude -->
Launch the researchers as background subagents with the Agent tool, in parallel (one message, multiple Agent calls) — at most six per pass without the user's go-ahead; when more questions wait, run the six highest-priority and ask before a second fan-out. Wait for every researcher to finish or fail — when the platform reports one hung, when one stays silent long after all its siblings returned, or when one passes ten minutes with no result, count it failed and move on; one researcher never holds the pass hostage — then compile once, naming every gap; never report results while researchers still run.

**Spawning researchers:**

**MUST:**

1. You **MUST** spawn every researcher with `model: "sonnet"` — never the session model.
2. You **MUST** spawn every researcher as the `general-purpose` subagent type, restricted by prompt to research plus one research-brief write.
3. You **MUST** ground every researcher with web search, carry the whole research brief contract in its prompt as **MUST:** / **MUST NOT:** lists, and require the research brief to take the template below.
4. You **MUST** require a dated source for every claim, and keep every field optional — "none" is a valid entry.
5. You **MUST** require the researcher's reply to carry only the research brief's file path and an abstract of at most three sentences — the full research brief lives in the file.
<!-- @end -->
<!-- @port codex pi
Without background subagents, run the web searches yourself, one question at a time, and write each question's research brief to its file in the template below — a dated source for every claim, every field optional ("none" is valid). Your own reading is the digest's source verification — do not re-open sources you just read.
-->

Required research brief template:

```markdown
## Findings

1. **Claim:** <one sentence>
  - **Evidence:** <what supports it>
  - **Source:** <name or URL, date>

(one entry per claim)

## Conflicts
<disagreements between sources, or "none">

## Confidence
<one line: how settled this is, and what would change it>
```

**Compiling the digest:** read every research brief file and validate it — open the sources behind the load-bearing claims and check them; a claim whose source cannot be opened is marked unverified in the digest, never silently promoted. Resolve conflicts by source authority and recency. Then report one digest: per question, the settled answer in one or two sentences, the confidence, any conflict worth surfacing, and the research brief's file path — and quote a research brief's relevant lines whenever the user asks; the files are theirs to read. A researcher that fails is reported, and the digest compiles from the research briefs that landed, naming the gap. A conflict the sources cannot settle routes by its subject: observable claims fall to Experiment; the rest is surfaced to the user in the digest with your best-supported reading — informing them of a conflict is not asking them a fact.

**Exploratory search.** The exploratory search is the web-wide search under Ask's shortcut duty: research whether a shortcut to the goal exists, even one that breaks settled design. Surface a found shortcut as a proposal with its evidence — the user rules; never silently displace settled design.

## Potential Step: Experiment

**When to use:**

1. Research finds that nothing existing holds a verifiable fact's answer and no local probe can reach it.
2. Sources conflict on an observable claim the digest cannot settle — a trial settles what documents dispute.
3. The user wants a judgment informed by blind evidence — candidates compared without their identities attached.

**MUST:**

1. You **MUST** invoke the `experiment` skill (it ships beside this one) for comparable candidates — blind candidates, blind verdicts, the user rules. (The skill shares this step's name: it is the step's blind-comparison branch, not a different thing.)
2. You **MUST** build, for a measurement needing setup beyond a quick local probe, the smallest rig that yields the observation.
3. You **MUST** run every probe and trial against the real system, and produce every candidate from it — never a stub built from memory.
4. You **MUST** record every trial's command and output beside the research briefs — created evidence is evidence, and the files are the user's to check.
5. You **MUST** get the user's go-ahead before a trial that would spend real money or touch systems beyond this machine.

**MUST NOT:**

1. You **MUST NOT** experiment on what research already settled — creation is the last source, not a shortcut around reading.

## The Pass

A pass is one design discussion's exploration, from the first step that fires to the last; it is over when no step's condition holds.
A step's output scales with what it finds:
- Ask on a well-framed question may add a single entry to the open list, and that is a completed step, not a skipped one.
- A user preference surfacing outside any open question is recorded as a ruling in Ask's written summary and applied where it bears.
  - The recording is the whole pass; no other step fires for it.

Worked examples:

<PASS_EXAMPLES>
- "What is 2^20?" — memory's strong form: derive it in-thread.
- "Does the installed v3 of library X preserve order?" — its behavior: this machine; its documented promise: the web.
- "Two docs disagree on the API's rename semantics." — observable: a trial settles it, not the user.
- "Which error message reads better?" — judgment: the user rules; an experiment prepares blind evidence when they want it.
- "Which browsers must we support?" — a private fact when the policy is already set (the user recites it); a judgment when it is being decided now (prepare it); when unsure which, prepare it.
- "What is p95 latency on staging?" — an environment only the user can grant: ask for access, then observe.
- "How much launch traffic should we provision for?" — split: research the base rates; the user rules the risk.
</PASS_EXAMPLES>

## Presenting

At the end of a full pass, present:
- The current understanding of purpose and intent;
- The alternatives explored and what each revealed;
- The strongest shortcut found;
- The recommendation and its rationale;
- What remains unverified, assumed, or parked
  - Facts, evidence, judgments, assumptions, and recommendations each labeled as what they are.

**MUST NOT:**

1. You **MUST NOT** preserve an earlier conclusion out of politeness, consistency, or sunk cost.
2. You **MUST NOT** let skepticism become endless doubt: when the evidence suffices, decide.
3. You **MUST NOT** hide evidence that weakens the recommendation.

## Invariants

**MUST:**
- You **MUST** ask a private fact plainly instead of researching around it;
- You **MUST** state every skipped source;
- You **MUST** verify load-bearing recalls before the recommendation rests on them.

**MUST NOT:**
- You **MUST NOT** ask the user a verifiable fact — at most ask them to route one;
- You **MUST NOT** silently assume a judgment;
- You **MUST NOT** put an unsorted question to the user;
- You **MUST NOT** answer for the system under study within reach from beliefs when it can be observed;
- You **MUST NOT** spend the web or an experiment on what memory, this machine, or one sentence from the user settles — except the verification a load-bearing recalled fact is owed, which is always permitted.
