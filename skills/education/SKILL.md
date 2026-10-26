---
name: education
description: "Use when producing learning material that teaches the user a topic, paper, system or result, so the user can understand and explain it afterwards."
---

# Educate

Use the `/communicate` skill to communicate with the user. Aim to get the reader to understand and be able to explain the subject afterwards. This skill is the learning-material counterpart of `presentation`: where `presentation` reports work progress with concerns, consequences and recommended actions, `education` teaches with the points below.

**Cover (not limited to these):**

1. **Learning goal.** State first what the reader will be able to explain or do after reading, from a top-down view.
2. **Why it matters to the reader.** Tie the subject to the reader's own products, decisions or work.
3. **Prerequisites and terms.** Assume the reader may not know the field's vocabulary. Define each term in plain words at first use, using the established term, and collect them in a glossary.
4. **Concepts, one at a time.** Order them from the whole to the parts. For each concept give a plain explanation, a concrete example, an illustration or something interactive to explore, and a quick self-check with immediate feedback.
5. **Common misconceptions and how to read critically.** Present limits and uncertainty as things to learn (for example how to read a preprint with caution, or why a sampled number is not a census), not as a risk report.
6. **Recap.** List what the reader should now be able to explain, as a checklist of complete sentences.
7. **Where to learn next.** Offer further reading or practice as optional learning paths, not as action items.

**MUST:**

1. You **MUST** ask with the tool dedicated for asking user questions **IF** you come to ask the user for questions **AND** the tool is available.
2. You **MUST** follow `/communicate`, including the illustrated, interactive HTML document when text alone would be tedious or ambiguous, and `/communication-consistency` for identifiers and measured numbers.

**MUST NOT:**

1. You **MUST NOT** frame learning material as a progress report, and **MUST NOT** add concerns, consequences or recommended-action blocks unless the user asks for them.
2. You **MUST NOT** pad the material with topics beyond the learner's stated goal.
