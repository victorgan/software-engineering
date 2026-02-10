# 🌳 Software Engineering — Tree of Knowledge

> A comprehensive map of every major concept area in software engineering.
> Use this as your home base. Each link leads to a deeper branch of the tree.

---

## 🧱 1. Foundations
*The roots — CS fundamentals everything else is built on.*

- [[01 - Foundations MOC]]
  - [[Data Structures]] — [[Arrays]], [[Linked Lists]], [[Tree Structures|Trees]], [[Graph Structures|Graphs]], [[Hash-Based Structures|Hash Maps]], [[Heaps]], [[Tries]]
  - [[Algorithms]] — [[Sorting]], [[Searching]], [[Graph Algorithms]], [[Dynamic Programming]], [[Greedy Algorithms|Greedy]], [[Backtracking]]
  - [[Computational Complexity]] — [[Big-O Notation|Big-O]], [[P vs NP Problem|P vs NP]], [[Space Complexity]], [[Amortized Analysis]]
  - [[Mathematics for CS]] — [[Discrete Mathematics|Discrete Math]], [[Linear Algebra]], [[Probability]], [[Statistics]], [[Information Theory]], Queueing Theory

---

## 💻 2. Programming Languages & Paradigms
*How we express computation — the tools of thought.*

- [[02 - Programming Languages and Paradigms MOC]]
  - [[Programming Paradigms]] — Imperative, OOP, Functional, Logic, Concurrent
  - [[Concurrency]] — Threads, Locks, [[Async-Await|Async/Await]], [[Actor Model]], CSP, [[Lock-Free & Wait-Free Programming|Lock-Free Programming]]
  - [[Type Systems]] — [[Static vs Dynamic Typing|Static vs Dynamic]], [[Strong vs Weak Typing|Strong vs Weak]], [[Type Inference]], Generics, [[Algebraic Data Types|Algebraic Types]]
  - [[Language Implementation]] — Compilers, Interpreters, JIT, ASTs, Parsing, [[Bytecode]]
  - [[Memory Models]] — [[Stack vs Heap]], Garbage Collection, [[Reference Counting]], Ownership (Rust), Manual Management

---

## 🗄️ 3. Data Management
*Storing, retrieving, and moving data — the lifeblood of applications.*

- [[03 - Data Management MOC]]
  - [[Relational Databases]] — SQL, [[Normalization]], [[Joins]], [[Indexing]], [[Query Optimization]], Transactions
  - [[NoSQL Databases]] — [[Document Stores|Document]], [[Key-Value Stores|Key-Value]], [[Column-Family Stores|Column-Family]], [[Graph Databases|Graph]], [[Time-Series Databases|Time-Series]]
  - [[Database Selection Guide]] — [[Decision Factors]], Tradeoffs, Polyglot Persistence Patterns
  - [[Data Modeling]] — [[ER Diagrams]], Schema Design, [[Denormalization]], [[Migrations]]
  - [[Caching]] — Strategies, [[Redis]], [[Memcached]], [[CDN Caching]], [[Cache Invalidation]]
  - [[Data Pipelines]] — [[ETL vs ELT|ETL/ELT]], Streaming vs Batch, Kafka, [[Data Lake|Data Lakes]], [[Data Warehouse|Data Warehouses]]
  - [[Database Operations]] — [[Connection Pooling]], Query Analysis, Maintenance, [[Backup and Restore|Backups]], Schema Migrations
  - Search Systems — Inverted Indexes, Text Analysis, Ranking, Full-Text Search, Vector Search
  - Data Serialization Formats — JSON, Protobuf, Avro, Parquet, Arrow, Schema Registries

---

## ⚙️ 4. Systems & Infrastructure
*The machines, networks, and platforms that run our software.*

- [[04 - Systems and Infrastructure MOC]]
  - [[Operating Systems]] — Processes, Threads, [[Memory Management]], [[File Systems]], I/O, Scheduling
  - [[Networking]] — TCP/IP, [[HTTP]], [[DNS]], [[TLS and SSL|TLS]], [[Load Balancing]], [[CDN|CDNs]], [[WebSockets]]
  - [[Distributed Systems]] — [[Consensus Algorithms|Consensus]], [[CAP Theorem]], [[Replication]], Sharding, [[Message Queues and Event Systems|Message Queues]]
  - [[Cloud and Containers]] — [[Docker]], [[Kubernetes]], [[Serverless]], [[Infrastructure as Code|IaC]]

---

## 🏗️ 5. Software Design & Architecture
*Structuring code and systems to be maintainable, scalable, and elegant.*

- [[05 - Software Design and Architecture MOC]]
  - [[OOP and SOLID Principles]] — [[Encapsulation]], [[Inheritance]], [[Polymorphism]], [[SOLID Principles|SOLID]], [[Composition vs Inheritance]]
  - [[Design Patterns]] — [[Creational Patterns|Creational]], [[Structural Patterns|Structural]], [[Behavioral Patterns|Behavioral]] (Gang of Four + Modern)
  - [[Architectural Patterns]] — [[Monolith]], [[Microservices]], [[Event-Driven Architecture|Event-Driven]], [[Layered Architecture|Layered]], [[Hexagonal Architecture|Hexagonal]], [[CQRS]]
  - [[API Design]] — [[REST]], [[GraphQL]], [[gRPC]], [[WebSockets]], [[API Versioning]], [[Rate Limiting]]
  - [[Domain-Driven Design]] — [[Bounded Contexts]], [[Aggregates]], [[Entities]], [[Value Objects]], [[Ubiquitous Language]]
  - [[System Design Tradeoffs]] — Consistency vs Availability, SQL vs NoSQL, [[Monolith vs Microservices Decision|Monolith vs Microservices]], Build vs Buy

---

## 🔧 6. Development Process
*The practices and tooling that make teams effective.*

- [[06 - Development Process MOC]]
  - [[Version Control]] — [[Git Internals]], Branching Strategies, [[Monorepo vs Polyrepo|Monorepos vs Polyrepos]]
  - [[Testing]] — [[Unit Testing|Unit]], [[Integration Testing|Integration]], E2E, [[Property-Based Testing|Property-Based]], TDD, Mocking, [[Fuzzing]]
  - [[CI-CD]] — Pipelines, [[Deployment Strategies]], [[Feature Flags]], Environments
  - [[Methodologies]] — [[Agile]], [[Scrum]], [[Kanban]], [[Extreme Programming]], [[Shape Up]]
  - [[Code Quality]] — [[Code Review]], Linting, [[Static Analysis and Linting|Static Analysis]], [[Refactoring]], [[Technical Debt]]

---

## 🛡️ 7. Reliability & Operations
*Keeping systems running — the art of not being paged at 3am.*

- [[07 - Reliability and Operations MOC]]
  - [[Observability]] — [[Logging]], [[Metrics]], Tracing, Dashboards, Alerting
  - [[Incident Management]] — [[On-Call]], [[Runbooks]], Post-Mortems, [[Blameless Culture]]
  - [[Site Reliability Engineering]] — [[SLAs, SLOs, SLIs]], [[Error Budgets]], [[Toil Management|Toil Reduction]], [[Production Readiness Reviews|Production Readiness]]
  - [[Disaster Recovery and Business Continuity]] — [[Backup and Restore|Backup/Restore]], [[Failover]], [[Disaster Recovery Tiers|DR Tiers]], [[RPO (Recovery Point Objective)|RPO]]/[[RTO (Recovery Time Objective)|RTO]]
  - [[Traffic Management]] — [[Traffic Shifting]], [[Load Shedding]], [[Dynamic Configuration]]
  - [[Performance Engineering]] — [[Profiling]], [[Benchmarking]], [[Load Testing]], [[Capacity Planning]], [[Chaos Engineering]]
  - Cost Engineering / FinOps — Cloud Costs, Right-Sizing, Reserved Capacity, Spot Instances, Unit Economics

---

## 🔐 8. Security
*Protecting systems, data, and users from harm.*

- [[08 - Security MOC]]
  - [[Cryptography]] — [[Hashing]], [[Symmetric Encryption|Symmetric]]/[[Asymmetric Encryption|Asymmetric Encryption]], [[TLS and SSL|TLS]], [[Digital Signatures]], [[PKI (Public Key Infrastructure)|PKI]]
  - [[Authentication and Authorization]] — [[OAuth 2.0]], OIDC, [[JWT (JSON Web Tokens)|JWT]], [[RBAC]], [[ABAC]], [[SSO (Single Sign-On)|SSO]], MFA
  - [[Application Security]] — [[OWASP Top 10]], [[Input Validation]], XSS, CSRF, [[SQL Injection]], SSRF
  - [[Infrastructure Security]] — [[Network Security]], [[Secrets Management]], [[Zero Trust Architecture|Zero Trust]], [[Container Security]]
  - [[Supply Chain Security]] — [[SLSA Framework|SLSA]], [[SBOM]], Dependency Scanning, [[Artifact Signing]]
  - [[Compliance and Privacy]] — [[GDPR]], [[SOC 2]], [[HIPAA]], [[PCI-DSS]], [[Privacy Engineering]]
  - [[Security Operations]] — [[Vulnerability Management]], [[SIEM]], [[Penetration Testing]], [[Red Team vs Blue Team|Red/Blue Team]]

---

## 🤖 9. Machine Learning & AI
*Teaching machines to learn — increasingly core to engineering.*

- [[09 - Machine Learning and AI MOC]]
  - [[ML Fundamentals]] — [[Supervised Learning|Supervised]], [[Unsupervised Learning|Unsupervised]], [[Reinforcement Learning]], [[Bias-Variance Tradeoff|Bias-Variance]], Evaluation
  - [[Deep Learning]] — [[Neural Network Fundamentals|Neural Networks]], [[Convolutional Neural Networks|CNNs]], [[Recurrent Neural Networks|RNNs]], [[Transformers]], [[GANs]], [[Diffusion Models]]
  - [[Natural Language Processing]] — [[Tokenization]], [[Embeddings]], [[Large Language Models|LLMs]], RAG, [[Fine-Tuning LLMs|Fine-Tuning]], [[Prompt Engineering]]
  - [[MLOps]] — [[Model Serving]], [[Feature Stores]], [[Experiment Tracking]], [[Model Monitoring]], [[Data Versioning]]
  - [[ML System Design]] — Batch vs Real-Time, [[Recommendation System Design|Recommendation Systems]], [[Search Ranking Design|Search Ranking]], [[Responsible AI]]

---

## 👥 10. Human & Organizational
*Software is a team sport — the people side of engineering.*

- [[10 - Human and Organizational MOC]]
  - [[Technical Communication]] — Documentation, [[ADRs]], [[RFCs]], [[Diagramming]], [[Writing for Engineers]]
  - [[Engineering Management]] — [[Team Topologies]], [[Tech Lead vs Engineering Manager|Tech Lead vs Manager]], [[Hiring and Growing Engineers|Hiring]], [[One-on-Ones|1-on-1s]], [[Planning and Execution|Planning]]
  - [[Engineering at Scale]] — [[Platform Engineering]], [[Technical Governance]], [[Staff Engineer Archetypes|Staff Archetypes]], [[Organizational Antipatterns|Org Antipatterns]]
  - [[Career Development]] — IC vs Management Track, [[System Design Interviews]], [[Open Source Participation|Open Source]], Google Interview Prep

---

## ☁️ 11. Cloud Providers & Proprietary Systems
*Vendor-specific services and internal platforms — proprietary instances of the concepts above.*

- [[11 - Cloud Providers and Proprietary Systems MOC]]
  - [[AWS Services Guide]] — Compute, Storage, Databases, Networking, Messaging, ML, Security
  - [[GCP Services Guide]] — Compute, Storage, Databases, Networking, Data Analytics, ML, Security
  - [[AWS vs GCP Service Mapping]] — Side-by-side service equivalents
  - [[Google Internal Technologies]] — [[Borg]], [[Spanner Internal|Spanner]], [[Bigtable]], [[Dremel]], [[Stubby]], [[Zanzibar]], [[BeyondCorp]]
  - [[Google Internal to External Mapping]] — Internal ↔ Open Source ↔ GCP equivalents

---

## 🌐 12. Web & Mobile Development
*Building user-facing applications — the most visible layer of our work.*

- [[12 - Web and Mobile Development MOC]]
  - [[Web Fundamentals]] — HTML, CSS, DOM, Browser Rendering Pipeline, Critical Rendering Path
  - [[JavaScript & the Browser]] — Event Loop, Web APIs, Web Workers, Service Workers, Module Systems
  - [[Frontend Frameworks]] — React, Vue, Angular, Svelte, Signals, State Management, SSR/CSR/SSG
  - [[Web Performance]] — Core Web Vitals, Lighthouse, Code Splitting, Image Optimization, Tree Shaking
  - [[Build Tooling]] — Webpack, Vite, esbuild, Turbopack, Babel, SWC, PostCSS, Tailwind, Monorepo Tools
  - [[Accessibility]] — WCAG, ARIA, Semantic HTML, Screen Readers, Keyboard Navigation
  - [[Browser APIs & PWAs]] — Service Workers, Cache API, Web Push, Offline-First, WebSockets, WebRTC
  - [[Frontend Testing]] — Testing Library, Visual Regression, Playwright, Cypress, Storybook
  - [[Mobile Development]] — iOS (Swift, SwiftUI), Android (Kotlin, Compose), React Native, Flutter, App Distribution
  - [[Internationalization]] — Unicode, ICU Message Format, Locale-Aware Formatting, RTL, Time Zones

---

## 🛠️ 13. Developer Tooling & Productivity
*The tools that multiply developer effectiveness — mastering them is a career-long leverage multiplier.*

- [[13 - Developer Tooling and Productivity MOC]]
  - [[Editors & IDEs]] — VS Code, JetBrains, Vim/Neovim, Emacs, LSP, DAP
  - [[Shell & Terminal]] — Bash/Zsh, Shell Scripting, Dotfiles, tmux, Modern CLI Tools
  - [[Debugging]] — Interactive Debuggers, Memory Debuggers, Profilers, Log-Based Debugging
  - [[Package Managers]] — npm/yarn/pnpm, pip/uv/poetry, Cargo, Go Modules, Maven/Gradle
  - [[Containers for Development]] — Dev Containers, Docker Compose, Testcontainers
  - [[AI-Assisted Development]] — Code Completion, Chat-Based Coding, AI Code Review, Limitations

---

## 🗺️ How to Use This Vault

1. **Start here** — Browse the tree to find what interests you
2. **Go deep** — Each MOC links to detailed topic notes
3. **Build connections** — Add your own notes and link them with `[[wiki-links]]`
4. **Track progress** — Use tags like `#learned`, `#in-progress`, `#to-study`
5. **Use Graph View** — Obsidian's graph view will visualize your knowledge tree

> 💡 This vault is a *starting scaffold*. The real value comes when you fill in the notes with your own understanding, examples, and connections.

---

## 🧬 Ontology

This vault organizes knowledge at four levels of specificity. Each MOC follows this hierarchy:

| Level | Term | Description | Example |
|---|---|---|---|
| 1 | **Domain** | Broadest subject area. Each numbered section is a domain. | Data Structures |
| 2 | **Category** | A grouping within a domain. Represented as H2/H3 headings in MOCs. | Linear Structures |
| 3 | **Concept** | A specific, nameable thing. The bolded terms in bullet points. | Arrays |
| 4 | **Sub-Concept** | A variant, detail, or sub-topic within a concept. The descriptions after the em dash. | contiguous memory, O(1) random access, B-Trees, DAGs |

**Domain → Category → Concept → Sub-Concept**

This terminology comes from ontology (knowledge representation). Alternate terms you may encounter:
- Domain = field, discipline
- Category = class, subclass, subdivision
- Concept = topic, entity
- Sub-Concept = variant, detail, attribute, facet
