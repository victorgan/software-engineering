# Conventions

Rules for authoring and formatting notes in this vault.

---

## File Naming

- **Title Case with spaces**: `Load Balancing Algorithms.md`, `Dependent Types.md`
- **H1 title must match filename exactly**
- **Hyphens** for compound concepts: `Write-Behind (Write-Back).md`, `Cache-Aside (Lazy Loading).md`
- **Parentheses** for disambiguation or alternate names: `Sum Types (Tagged Unions).md`
- **Ampersands** for tightly coupled pairs: `Closures & Currying.md`, `Classes & Objects.md`
- **Acronyms** preserve original casing: `ACID Properties.md`, `gRPC.md`, `mTLS.md`, `eBPF.md`
- No underscores in filenames

## Folder Naming

- **Domains**: `NN Domain Name` — two-digit zero-padded prefix, Title Case
  - `01 Foundations`, `04 Systems and Infrastructure`
- **Sub-domains**: `NN Sub-Domain Name` — sequential numbering starting at `00`
  - `00 Data Structures`, `01 Algorithms`, `02 Computational Complexity`
- **Hierarchy folders**: Three fixed names at the leaf level
  - `00 Category` — groupings within a sub-domain
  - `01 Concept` — specific, nameable topics
  - `02 Sub-Concept` — variants, details, facets of a concept

## Note Templates

### Leaf Note (Concept / Sub-Concept)

```markdown
# Topic Title

> <- Back to [[Parent Category]]

Brief 1-2 sentence description of the concept.

## Key Properties

- [[Sub-topic 1]]
- [[Sub-topic 2]]
- [[Sub-topic 3]]

## Related

- [[Related Concept 1]]
- [[Related Concept 2]]

---

#tag1 #tag2
```

### Hub Note (Category Level)

```markdown
# Category Name

> <- Back to [[Parent Sub-Domain]]

1-2 sentence description of the category's purpose.

## Concepts

- [[Concept 1]]
- [[Concept 2]]
- [[Concept 3]]

---

#tag1 #tag2
```

### Map of Content (MOC)

```markdown
# NN - Domain Name MOC

> <- Back to [[Software Engineering - Map of Content]]

Opening paragraph explaining domain importance.

---

## [[Major Category 1]]

### Subcategory
- **[[Concept]]** — Inline description with context
- **[[Another Concept]]** — Description continues here

---

## [[Major Category 2]]

...

---

#domain-tag
```

## Back-Links

- **Format**: `> <- Back to [[Parent Note]]`
- Every note must have exactly one back-link on line 3 (after the H1 and blank line)
- MOC files link back to `[[Software Engineering - Map of Content]]`
- Category notes link back to their sub-domain folder note
- Concept/Sub-Concept notes link back to their parent category

## Tags

- **Placement**: End of file, after a horizontal rule (`---`)
- **Format**: `#kebab-case` — all lowercase, hyphens between words
- **Count**: 2-4 tags per concept note, 1-2 per MOC
- **Hierarchy**: Domain tag first, then narrower topic tags
  - Example: `#data-structures #hashing #hash-tables`
- **Acronyms** stay lowercase: `#ddd`, `#cicd`, `#aws`, `#gcp`

## Linking

- Use `[[wiki-links]]` for all internal references
- **Key Properties** section: list sub-topics as bare links (`- [[Topic]]`)
- **Related** section: links with optional brief context (`- [[Topic]] — why it's related`)
- **MOC** bold-link pattern: `**[[Concept]]** — description after em dash`
- Link to existing notes whenever a concept is mentioned; do not leave unlinked references

## Content Depth

| Note Type     | Lines  | Key Properties | Related | Description       |
|---------------|--------|----------------|---------|-------------------|
| Sub-Concept   | 5-15   | Optional       | Optional| 1 sentence        |
| Concept       | 20-35  | Required       | Required| 1-3 sentences     |
| Category Hub  | 12-20  | —              | Optional| 1-2 sentences     |
| MOC           | 150-450| —              | —       | 1 paragraph       |

## Folder Notes

Sub-domain folders may contain a **folder note** — a file named identically to the folder (minus the number prefix). This serves as the entry point for that sub-domain.

Example: `01 Foundations/03 Mathematics for CS/Mathematics for CS.md`

## Horizontal Rules

- Use `---` to separate the main content from the tag footer
- In MOCs, use `---` between major H2 sections for visual separation
