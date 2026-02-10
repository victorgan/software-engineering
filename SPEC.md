# Vault Specification

Architecture, ontology, and structural rules for the Software Engineering knowledge base.

---

## Purpose

A comprehensive, interlinked knowledge base covering the full breadth of software engineering. Designed for use in Obsidian as a navigable tree of ~3,000 notes connected by wiki-links.

## Ontology

Knowledge is organized at four levels of specificity:

| Level | Term           | Description                                              | Example                        |
|-------|----------------|----------------------------------------------------------|--------------------------------|
| 1     | **Domain**     | Broadest subject area. Each numbered section is a domain | Data Management                |
| 2     | **Category**   | A grouping within a domain                               | Caching                        |
| 3     | **Concept**    | A specific, nameable thing                               | Cache-Aside                    |
| 4     | **Sub-Concept**| A variant, detail, or sub-topic within a concept         | Time-Based Expiration          |

**Alternate terminology**:
- Domain = field, discipline
- Category = class, subdivision
- Concept = topic, entity
- Sub-Concept = variant, detail, attribute, facet

## Domain Registry

| #  | Domain                                    | Status   |
|----|-------------------------------------------|----------|
| 00 | MOC (root index)                          | Complete |
| 01 | Foundations                               | Complete |
| 02 | Programming Languages and Paradigms       | Complete |
| 03 | Data Management                           | Complete |
| 04 | Systems and Infrastructure                | Complete |
| 05 | Software Design and Architecture          | Complete |
| 06 | Development Process                       | Complete |
| 07 | Reliability and Operations                | Complete |
| 08 | Security                                  | Complete |
| 09 | Machine Learning and AI                   | Complete |
| 10 | Human and Organizational                  | Complete |
| 11 | Cloud Providers and Proprietary Systems   | Complete |
| 12 | Web and Mobile Development                | Stub     |
| 13 | Developer Tooling and Productivity        | Stub     |

## Directory Layout

```
software-engineering/
├── .obsidian/                          # Obsidian config, plugins, themes
├── 00 MOC/
│   └── Software Engineering - Map of Content.md   # Root entry point
├── NN Domain Name/                     # One per domain (01-13)
│   ├── NN - Domain Name MOC.md         # Domain-level Map of Content
│   ├── NN Sub-Domain Name/             # One per major topic area
│   │   ├── Sub-Domain Name.md          # Optional folder note (entry point)
│   │   ├── 00 Category/               # Category-level notes
│   │   ├── 01 Concept/                # Concept-level notes
│   │   └── 02 Sub-Concept/            # Sub-Concept-level notes
│   └── ...
├── BACKLOG.md                          # Planned improvements and sources
├── CONVENTIONS.md                      # Authoring rules and formatting
├── SPEC.md                             # This file
└── STYLE_GUIDE.md                      # Writing style and content guidelines
```

## Navigation Model

```
Software Engineering - Map of Content
  │
  ├── NN - Domain MOC
  │     │
  │     ├── Category hub note
  │     │     ├── Concept note
  │     │     │     ├── Sub-Concept note
  │     │     │     └── Sub-Concept note
  │     │     └── Concept note
  │     └── Category hub note
  │           └── ...
  └── NN - Domain MOC
        └── ...
```

- **Downward**: MOC -> Category -> Concept -> Sub-Concept (via `[[wiki-links]]`)
- **Upward**: Every note has a back-link to its parent (`> <- Back to [[Parent]]`)
- **Lateral**: "Related" sections cross-link between notes in different domains

## Note Types

### Root MOC
- **Count**: 1
- **Location**: `00 MOC/`
- **Role**: Single entry point linking to all 13 domain MOCs
- **Contains**: Hierarchical overview of all domains with inline concept links

### Domain MOC
- **Count**: 13 (one per domain)
- **Naming**: `NN - Domain Name MOC.md`
- **Location**: Root of the domain folder
- **Role**: Exhaustive outline of a domain; lists every category, concept, and sub-concept with brief descriptions
- **Structure**: H2 sections for major categories, H3 for subcategories, bold wiki-linked concepts with em-dash descriptions

### Folder Note
- **Location**: Root of a sub-domain folder, named to match the folder (minus number prefix)
- **Role**: Entry point and overview for a sub-domain
- **Example**: `03 Data Management/05 Caching/Caching.md`

### Category Note
- **Location**: `00 Category/`
- **Role**: Groups related concepts under a shared theme
- **Structure**: Back-link, description, list of child concepts

### Concept Note
- **Location**: `01 Concept/`
- **Role**: Primary knowledge unit; a specific, nameable topic
- **Structure**: Back-link, description, Key Properties, Related, tags

### Sub-Concept Note
- **Location**: `02 Sub-Concept/`
- **Role**: Variant, implementation detail, or facet of a concept
- **Structure**: Back-link, brief description, tags (may omit Key Properties)

## Link Graph Properties

- Every note has exactly one back-link (upward)
- Concept notes average 4-8 outgoing wiki-links
- MOC files contain 100-250+ outgoing wiki-links
- The graph forms a **lattice** — primarily tree-shaped with lateral cross-links via Related sections

## Metadata

- **No YAML frontmatter** — all files are pure markdown
- **Tags**: `#kebab-case` at end of file, after `---`
- **Back-links**: `> <- Back to [[Parent]]` on line 3

## Obsidian Configuration

Key settings (`.obsidian/app.json`):
- Vim mode enabled
- Auto-update links on file rename
- Alphabetical file sort
- Live preview mode
- Line numbers shown

Plugins: obsidian-git, dataview, calendar, folder-note-plugin, obsidian-linter, obsidian-kanban, and 20+ others (see `.obsidian/community-plugins.json`).
