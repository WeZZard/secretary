# Communication Consistency

## Using a Visual Glossary

**Use when:** the presentation names parts of a visual artifact that the user may not recognize, such as components, screens, or regions of an app.

1. You **MUST** include a visual glossary. A visual glossary is an annotated screenshot of the artifact that highlights and labels each part the presentation names.
2. You **MUST** label each highlighted part with the same human-readable name that the text uses.
3. You **MUST** take the screenshot from the running artifact rather than drawing it from memory.
4. You **MUST** highlight only the parts that the presentation names.

## Citing Identified Resources

**Use when:** you cite a resource whose identifier is defined in the project's documents, such as a requirement, a decision, or a user story recorded as `ID-1`.

An identifier alone carries no context. A reader who meets `ID-1` in a sentence must look it up before the sentence makes sense.

1. You **MUST** cite the resource with a human-readable description, followed by a reference to its identifier.
2. You **MUST** take the description from the resource's title or its own wording in the project's documents.
3. You **MUST** use the same description for the same resource every time.
4. You **MUST** add the reference only at the first mention of the resource in each reply or document.
5. You **MUST** give the identifier in the reference, which is a footnote or an appendix entry, and say where the identifier is defined.
6. You **MUST** cite the identifier that the project's documents already define, rather than assign a new one.
7. You **MUST NOT** cite the resource by its identifier alone, such as "This change satisfies ID-1."

A table in an appendix or a reference section, such as a traceability matrix, may list identifiers in their own column.

For example:

```markdown
Requests on the checkout page must not wait for analytics to finish[^checkout-analytics]. The analytics call therefore moves to a background queue.

...

The retry policy also keeps requests on the checkout page from waiting for analytics to finish.

[^checkout-analytics]: `ID-1`, defined in docs/requirements.md.
```

## Using Stable Measurements

**Use when:** presenting measured data.

**One formula per quantity, for the whole session.**

You **MUST** pick the formula once and use it for every model, every configuration and every comparison from then on when you report a measured number.
You **MUST NOT** switch formula between turns, between sections of a document, or to make a comparison come out.

**Using established formula over inventing new formula.**

You **MUST** look for appropriate established formula before inventing your own.

**Naming the formula wherever a number appears.**

A bare unit is not a label. "tok/s" is not a measurement; "served rate, tok/s" and "decode rate, tok/s" are.

If two formulas both have a claim to a name, define both once, in one place, and refer back to it.

**Two numbers that came from different formulas are different quantities.**

Do not put them in the same table, the same sentence, or the same comparison.

The fact that one can be derived from the other does not make them comparable — it makes the difference explainable, which is not the same thing.

**When an outside number was measured under different conditions, fix the measurement, not the formula.**

Switching formula so a comparison lines up is the failure this rule exists to stop.

Match the conditions and measure again, or state plainly that the comparison is not like-for-like and say why.
