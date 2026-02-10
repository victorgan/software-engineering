# Style Guide

Writing style and content guidelines for notes in this vault.

---

## Voice and Tone

- **Concise and declarative**. State what something *is*, not what it "can be thought of as."
- **Technical but accessible**. Assume the reader is an engineer, not a beginner — but define non-obvious terms.
- **Neutral reference tone**. No first person, no conversational filler. Write like a reference card, not a tutorial.

Good: "Raft elects a leader through randomized election timeouts."
Bad: "So basically, Raft is a way to pick a leader using timeouts."

## Descriptions

- **Concept notes**: 1-3 sentences. State what it is, why it matters, and its key tradeoff or property.
- **Sub-Concept notes**: 1 sentence. Define it in terms of its parent concept.
- **Category notes**: 1-2 sentences. State what the grouping covers and why it's a coherent unit.
- **MOC opening paragraphs**: 2-4 sentences. Frame the domain's scope and importance to software engineering.

## Concept Descriptions — Pattern

Follow this structure for the opening description of a concept note:

```
[What it is]. [Key property or mechanism]. [Primary tradeoff, use case, or distinguishing detail].
```

Example:
> A hash table maps keys to values using a hash function for constant-time average lookup. Collisions are resolved via chaining or open addressing. Performance degrades to O(n) in the worst case when many keys hash to the same bucket.

## Bullet Points

- Start with the linked concept name: `- [[Topic Name]]`
- In MOCs, bold the link and follow with an em dash and description: `- **[[Topic]]** — description`
- In Key Properties sections, bare links are sufficient: `- [[Sub-topic]]`
- In Related sections, add brief context when the relationship is non-obvious: `- [[Bloom Filters]] — probabilistic alternative using hashing`

## Em Dash Usage

Use em dashes (`—`, not `--` or `-`) to separate concept names from their descriptions in MOC bullet points:

```markdown
- **[[Cache-Aside]]** — Application reads from cache first, loads from DB on miss
```

## Headings

- **H1**: Note title only. One per file. Must match filename.
- **H2**: Major sections within a note (`## Key Properties`, `## Related`, `## Complexity`)
- **H3**: Subcategories within MOC H2 sections
- Do not skip heading levels (no H1 -> H3)

## Standard Sections

Use these section names consistently:

| Section            | Used In           | Purpose                                      |
|--------------------|-------------------|----------------------------------------------|
| `## Key Properties`| Concept notes     | List sub-topics and defining characteristics |
| `## Related`       | Concept notes     | Cross-links to related concepts              |
| `## Complexity`    | Algorithm/DS notes| Time and space complexity table               |
| `## Concepts`      | Category hubs     | List of child concept notes                  |
| `## Categories`    | Hub notes         | List of child category notes                 |

Domain-specific sections are permitted when standard names don't apply (e.g., `## GCP Equivalent` in AWS service notes).

## Complexity Tables

For data structure and algorithm notes, use this format:

```markdown
## Complexity

| Operation | Average | Worst |
|-----------|---------|-------|
| Insert    | O(1)    | O(n)  |
| Lookup    | O(1)    | O(n)  |
| Delete    | O(1)    | O(n)  |
```

## What Not to Include

- **No code samples**. This is a concept reference, not a cookbook. Link to external resources if needed.
- **No lengthy prose**. If a description exceeds 3 sentences, consider splitting into sub-notes.
- **No duplicate content**. If two notes cover overlapping material, one should link to the other rather than repeat it.
- **No external links in note bodies**. Keep notes self-contained within the vault's wiki-link graph. External URLs belong in BACKLOG.md as sources to integrate.
- **No images or attachments** unless they add irreplaceable value (e.g., architecture diagrams).

## Capitalization

- **Note titles**: Title Case (`Load Balancing Algorithms`, not `load balancing algorithms`)
- **Tags**: all lowercase kebab-case (`#data-structures`, not `#Data-Structures`)
- **Headings**: Sentence case for H2/H3 (`## Key Properties`, `## Related`)
- **Acronyms**: Preserve standard casing (`ACID`, `gRPC`, `mTLS`, `eBPF`)

## Linking Discipline

- Link a term **on first mention** in a note. Do not link every occurrence.
- Prefer linking to the most specific note. Link to `[[AVL Trees]]` not `[[Tree Structures]]` when discussing AVL trees specifically.
- Do not create links to notes that don't exist unless you plan to create them immediately.
- Every concept note should have at least 3 outgoing links (excluding the back-link).
