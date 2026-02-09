# 10 — Human & Organizational MOC

> ← Back to [[Software Engineering - Map of Content]]

Software is built by people, for people, in organizations. The human side of engineering is often the difference between success and failure.

---

## [[Technical Communication]]

### Written Documentation
- **README** — Project purpose, setup, usage, contributing guidelines
- **API Documentation** — Endpoint reference, examples, error codes (OpenAPI/Swagger, Redoc)
- **Architecture Documentation** — System overview, component interactions, deployment topology
- **Architecture Decision Records (ADRs)** — Context, decision, consequences, status
- **RFCs (Request for Comments)** — Proposals for significant changes, gather feedback
- **Runbooks** — Step-by-step operational procedures (see [[Incident Management]])
- **Onboarding Docs** — Getting started guides, environment setup, codebase tour
- **Changelogs** — User-facing record of changes per release

### Writing for Engineers
- **Technical Writing Principles** — Clarity, conciseness, audience awareness, structure
- **Writing Good Bug Reports** — Steps to reproduce, expected vs actual, environment details
- **Writing Good PRs** — Context, what changed, why, how to test, screenshots
- **Commit Messages** — Conventional commits, imperative mood, explain why not just what
- **Writing RFCs** — Problem statement, proposed solution, alternatives considered, risks

### Diagramming
- **Sequence Diagrams** — Show interactions over time between components
- **Architecture Diagrams** — C4 Model (Context, Container, Component, Code)
- **Entity-Relationship Diagrams** — Data modeling (see [[Data Modeling]])
- **Flow Charts** — Process flows, decision trees
- **State Diagrams** — State machines, transitions
- **Tools** — Mermaid (code-based), Excalidraw, draw.io, Lucidchart, PlantUML

### Presentations & Communication
- **Technical Presentations** — Demo-driven, progressive disclosure, know your audience
- **Stakeholder Communication** — Translate technical concepts for non-technical audiences
- **Status Updates** — Concise, focus on blockers and progress, avoid jargon
- **Brag Documents** — Track your accomplishments for performance reviews

---

## [[Engineering Management]]

### Team Structure
- **Team Topologies** — Stream-aligned, enabling, complicated subsystem, platform teams
- **Conway's Law** — Organizations design systems that mirror their communication structure
- **Inverse Conway Maneuver** — Design teams to get the architecture you want
- **Two-Pizza Teams** — Small, autonomous teams (Amazon)
- **Staff+ Engineers** — Tech Lead, Staff, Principal, Distinguished — IC leadership track
- **Tech Lead vs Engineering Manager** — Technical direction vs people management

### Engineering Culture
- **Psychological Safety** — Safe to take risks, admit mistakes, ask questions
- **Blameless Culture** — Focus on systems, not individuals (see [[Incident Management]])
- **Developer Experience (DevEx)** — Fast builds, good tooling, minimal friction, developer productivity
- **Documentation Culture** — Write things down, institutional knowledge preservation
- **Knowledge Sharing** — Tech talks, guilds/chapters, brown bags, internal blogs
- **Open Source Participation** — Contributing, maintaining, licensing (MIT, Apache, GPL)

### Planning & Execution
- **Sprint Planning** — Estimation, prioritization, capacity (see [[Methodologies]])
- **Estimation Techniques** — Story points, t-shirt sizing, #NoEstimates, reference-based
- **Roadmapping** — Now/Next/Later, opportunity-solution trees, OKRs
- **OKRs (Objectives & Key Results)** — Alignment, measurable outcomes, ambitious targets
- **Project Management** — Gantt charts, dependency tracking, critical path
- **Risk Management** — Identify, assess, mitigate, monitor risks

### Hiring & Growing Engineers
- **Interviewing** — System design, coding, behavioral, take-home, pair programming
- **Leveling** — Engineering levels, competency matrices, expectations per level
- **1-on-1s** — Regular check-ins, career development, feedback, blockers
- **Performance Reviews** — Self-review, peer feedback, calibration
- **Mentorship** — Pairing senior + junior, structured vs organic mentoring
- **Onboarding** — 30/60/90 day plans, buddy system, ramp-up projects

### Engineering Metrics
- **DORA Metrics** — Deployment frequency, lead time for changes, MTTR, change failure rate
- **SPACE Framework** — Satisfaction, Performance, Activity, Communication, Efficiency
- **Goodhart's Law** — When a measure becomes a target, it ceases to be a good measure
- **Developer Productivity** — Qualitative + quantitative, avoid reductive metrics

---

## [[Career Development]]

### Individual Contributor Track
- **Junior Engineer** — Learning fundamentals, completing well-scoped tasks, asking questions
- **Mid-Level Engineer** — Independently delivering features, owning components, mentoring juniors
- **Senior Engineer** — System design, technical leadership, cross-team influence, setting standards
- **Staff Engineer** — Org-wide technical strategy, solving ambiguous problems, multiplying team output
- **Principal / Distinguished** — Company-wide or industry-wide impact, defining technical vision

### Core Skills by Level
- **Coding** — Clean code → maintainable systems → architectural decisions → technical strategy
- **System Design** — Component design → service design → distributed system design → platform architecture
- **Communication** — PRs & docs → technical presentations → cross-org influence → industry thought leadership
- **Leadership** — Self-management → team influence → org influence → company/industry influence

### System Design Interviews
- **Framework** — Requirements gathering → high-level design → deep dive → tradeoffs
- **Common Problems** — URL shortener, news feed, chat system, rate limiter, search autocomplete, notification system
- **Key Concepts** — Scalability, availability, consistency, partition tolerance, latency
- **Resources** — "Designing Data-Intensive Applications" (Kleppmann), "System Design Interview" (Alex Xu)

### Building Expertise
- **T-Shaped Skills** — Deep in one area, broad across many
- **Learning Strategies** — Build projects, read source code, contribute to open source, write about what you learn
- **Staying Current** — Conference talks, papers, blogs, newsletters, podcasts
- **Writing & Teaching** — Blog posts, talks, workshops — teaching deepens understanding
- **Side Projects** — Practical application, experimentation with new technologies

### Essential Books (a starting library)
- **Fundamentals** — "Introduction to Algorithms" (CLRS), "Structure and Interpretation of Computer Programs" (SICP)
- **Design** — "Design Patterns" (GoF), "Clean Code" (Martin), "Refactoring" (Fowler), "A Philosophy of Software Design" (Ousterhout)
- **Architecture** — "Designing Data-Intensive Applications" (Kleppmann), "Building Microservices" (Newman), "Fundamentals of Software Architecture" (Richards & Ford)
- **Systems** — "Computer Networking: A Top-Down Approach" (Kurose & Ross), "Operating Systems: Three Easy Pieces" (Arpaci-Dusseau)
- **Process** — "The Pragmatic Programmer" (Hunt & Thomas), "Accelerate" (Forsgren et al.), "The Phoenix Project" (Kim)
- **People** — "An Elegant Puzzle" (Larson), "The Manager's Path" (Fournier), "Staff Engineer" (Larson)
- **Thinking** — "Thinking in Systems" (Meadows), "The Design of Everyday Things" (Norman)

---

#career #management #communication #culture
