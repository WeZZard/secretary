---
name: get-audience-on-x
description: "Use before writing anything for an X account, and whenever the author's audience or self-image may have changed: refresh the local plain-text picture of who follows the author and who the author is and speaks for, then hand it to the writing skill, such as bridge-on-x."
---

# Get audience on X

Use the `/communicate` skill. The audience of an X account is a fact about the author, learned from data and then fixed. It is not something a writing skill invents for each post. This skill keeps two plain-text files up to date in the agent's persistent local folder `audience-on-x/`, and hands a short brief from them to other skills.

**Files** (plain natural language, no database; each starts with the date, the sources and how much was read, and ends with a short "changed since last time" note):

1. `audience.md`: who follows the author now.
2. `identity.md`: who the author is, what the author stands for and who the author speaks for.

**Update:**

1. **Followers.** With the author's own X connection, read-only, read the profile and the follower list as far as the API gives it, and state how many of the total were read and in what order. Never sign in through a browser, never use tokens or private endpoints. If the list cannot be read, say so and keep the last file.
2. **Classify.** Group followers by bio, name, location and language into categories you derive from the data. Report counts and shares, the language and location split, typical account size and activity, how many bios are empty or look automated, and the few most notable accounts. State the limits: sample size, keyword judgement, empty bios.
3. **Author.** Read the author's recent original posts, not reposts. Infer who the author believes they are, what they stand for, who they speak for, their recurring theses, and the tones and framings they would never use. Back each point with a short quote and mark it as inferred.
4. **Confirm.** Ask the author to confirm or correct both files. Keep their words in an "Author-confirmed" section that later updates never overwrite; it outranks anything inferred.
5. **Brief.** Finish with an audience brief of at most 120 words: who to write for with rough shares, who the author is and speaks for, and what to avoid. This is the output other skills use.

**Refresh** when the author asks, when a writing skill finds the files missing, or when they are more than 30 days old.

**MUST:**

1. You **MUST** treat the author's own statements about their audience and identity as final.
2. You **MUST** label every inference as an inference and every number with how it was computed.

**MUST NOT:**

1. You **MUST NOT** post, follow, like or message anything on X, or read bookmarks, likes or private messages.
2. You **MUST NOT** store tokens, or personal details about followers beyond public handles and bios.
3. You **MUST NOT** pick a different audience because a topic would suit one better.
