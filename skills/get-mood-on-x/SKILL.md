---
name: get-mood-on-x
description: "Use before writing anything for an X account, and whenever that read may have changed: get a fresh read on who the author is, whom the author speaks for, and who the audience is right now, then hand a short brief to the writing skill, such as bridge-on-x."
---

# Get mood on X

Use the `/communicate` skill. Mood means a read on who the author is, whom the author speaks for, and who the audience is right now. That read is a fact about the author, learned from data and then fixed. It is not something a writing skill invents for each post.

Keep one SQLite file, `mood-on-x/mood.sqlite`, in the agent's persistent local folder, on the agent's own machine and outside this repo. Public handles and bios only. The file holds four tables:

1. **Followers:** each follower seen, with handle, bio, the date first seen and the date last seen.
2. **Posts:** each of the author's original posts, with the date and the text.
3. **Statements:** each statement the author made himself about who he is, whom he speaks for and who his readers are, with the date.
4. **Runs:** each run, with the date, the sources and how many items were read.

**Each run:**

1. **Fetch.** With the author's own X connection, read-only, fetch new followers, new bios, and the author's new original posts, not reposts. Read the profile and the follower list as far as the connection gives them, and record how many of the total were read and in what order. Never sign in through a browser, and never use tokens or private endpoints. If a source cannot be read, say so and keep what is already stored.
2. **Store.** Add what was fetched. For a follower already stored, keep the first-seen date, write the new bio, and set last-seen to this run. Add posts that are not already stored. When the file is missing or empty, this run creates it.
3. **Read back.** Pull everything already collected, not only what this run just fetched.
4. **Evaluate.** Classify the followers. Give counts, and say how each count was made. Read the author's posts for what he stands for, and label that reading as inference unless he said it himself. Note what changed compared with the earlier runs, and reach a conclusion. The author's own statements always outrank anything inferred. The audience is fixed by the author and by the evidence in the database.
5. **Confirm.** Ask the author to confirm or correct, and record his answer as a new statement. Leave statements already stored as they are. When two statements disagree, the later one stands.
6. **Brief.** Hand the writing skill an audience brief of at most 120 words: who to write for, who the author is and speaks for, and what to avoid. The brief is the output of this run, not the record. The database is the record. Do not write the brief, or any conclusion, into this skill.

**Refresh** when the author asks, when a writing skill finds the database missing, or when the last run is more than 30 days old.

**MUST:**

1. You **MUST** treat the author's own statements about who he is, whom he speaks for and who his readers are as final.
2. You **MUST** label every inference as an inference and every number with how it was counted.

**MUST NOT:**

1. You **MUST NOT** post, follow, like or message anything on X, or read bookmarks, likes or private messages.
2. You **MUST NOT** store tokens, or personal details about followers beyond public handles and bios.
3. You **MUST NOT** pick a different audience because a topic would suit one better.
4. You **MUST NOT** put concrete audience or identity conclusions in this skill: no percentages, no named groups, no quotes from the author. Those come only from the database at run time.
