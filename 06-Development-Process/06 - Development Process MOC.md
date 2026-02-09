# 06 — Development Process MOC

> ← Back to [[Software Engineering - Map of Content]]

The practices, tools, and methodologies that make software teams effective. Process is what turns individual skill into collective capability.

---

## [[Version Control]]

### Git Internals
- **Object Model** — Blobs (files), Trees (directories), Commits (snapshots), Tags
- **SHA-1 Hashing** — Content-addressable storage, every object identified by hash
- **Refs** — Branches as pointers to commits, HEAD, tags
- **The DAG (Directed Acyclic Graph)** — Commit history as a graph
- **Packfiles** — Delta compression for efficient storage

### Git Workflows
- **Feature Branch Workflow** — Branch per feature, merge to main
- **Gitflow** — develop, feature, release, hotfix branches (heavier process)
- **Trunk-Based Development** — Short-lived branches, frequent integration to main
- **GitHub Flow** — Simple: branch, PR, review, merge to main
- **Ship/Show/Ask** — Categorize changes by review needs

### Branching & Merging
- **Merge Commits** — Preserve branch history, merge commit node
- **Rebase** — Linear history, replay commits on top of target
- **Squash Merge** — Compress branch into single commit
- **Cherry-Pick** — Apply specific commits to another branch
- **Conflict Resolution** — Manual merge, rerere, merge tools

### Monorepo vs Polyrepo
- **Monorepo** — All code in one repo (Google, Meta), shared tooling, atomic changes
- **Polyrepo** — Separate repo per service/library, independent versioning
- **Monorepo Tools** — Nx, Turborepo, Bazel, Pants, Lerna
- **Tradeoffs** — Visibility and refactoring ease (mono) vs independence and scaling (poly)

### Advanced Git
- **Git Hooks** — Pre-commit, pre-push, commit-msg (husky, pre-commit framework)
- **Git Bisect** — Binary search for bug-introducing commit
- **Git Worktrees** — Multiple working directories from one repo
- **Submodules & Subtrees** — Nested repositories
- **Large File Storage (LFS)** — Git LFS for binary assets

---

## [[Testing]]

### Testing Pyramid
- **Unit Tests** — Test individual functions/classes in isolation, fast, many
- **Integration Tests** — Test interactions between components, moderate speed
- **End-to-End (E2E) Tests** — Test full user flows, slow, fewer
- **The Trophy Model** — More integration tests, fewer unit and E2E (Kent C. Dodds)

### Unit Testing
- **Frameworks** — JUnit (Java), pytest (Python), Jest (JS), Go testing, RSpec (Ruby)
- **Assertions** — Equality, truthiness, exceptions, approximate values
- **Test Organization** — Arrange-Act-Assert, Given-When-Then
- **Test Naming** — Descriptive names that document behavior
- **Parameterized Tests** — Same test, multiple inputs

### Test Doubles
- **Mocks** — Verify interactions (method calls, arguments)
- **Stubs** — Return predetermined values
- **Fakes** — Working implementations (in-memory database)
- **Spies** — Record calls without changing behavior
- **Fixtures** — Shared test data setup/teardown

### Integration Testing
- **Database Tests** — Testcontainers, in-memory databases, transaction rollback
- **API Testing** — HTTP client tests, contract testing, WireMock
- **Component Testing** — Test a service with its real dependencies, mocked external services

### End-to-End Testing
- **Browser Testing** — Playwright, Cypress, Selenium
- **API E2E** — Full request/response through the system
- **Visual Regression** — Screenshot comparison (Percy, Chromatic)
- **Flaky Tests** — Causes, retries, quarantine strategies

### Advanced Testing Techniques
- **Test-Driven Development (TDD)** — Red-Green-Refactor cycle, design through testing
- **Behavior-Driven Development (BDD)** — Gherkin syntax, Cucumber, executable specifications
- **Property-Based Testing** — Generate random inputs, verify properties (Hypothesis, QuickCheck, fast-check)
- **Mutation Testing** — Modify code to verify tests catch bugs (PIT, Stryker)
- **Fuzzing** — Random/intelligent input generation to find crashes (AFL, libFuzzer)
- **Snapshot Testing** — Record output, detect unintended changes
- **Contract Testing** — Pact, verify API agreements between services
- **Chaos Testing** — See [[Performance Engineering]]
- **Load Testing** — See [[Performance Engineering]]

### Test Strategy
- **Code Coverage** — Line, branch, condition coverage; coverage as a metric (not a goal)
- **What to Test** — Business logic, edge cases, error paths, not implementation details
- **Test Maintenance** — Avoiding brittle tests, testing behavior not implementation
- **Testing in CI** — Parallel execution, test splitting, fail-fast

---

## [[CI-CD]]

### Continuous Integration (CI)
- **Core Practice** — Merge to main frequently, automated build + test on every push
- **Build Pipeline** — Checkout → Install → Lint → Test → Build → Publish
- **CI Tools** — GitHub Actions, GitLab CI, Jenkins, CircleCI, Buildkite, Drone
- **Build Artifacts** — Docker images, binaries, packages, test reports
- **Pipeline Optimization** — Caching, parallelism, incremental builds, affected-only testing

### Continuous Delivery / Deployment
- **Continuous Delivery** — Always releasable, manual deploy trigger
- **Continuous Deployment** — Every green build deploys automatically
- **Deployment Pipeline** — Build → Test → Staging → Production
- **Environments** — Dev, staging, pre-prod, production, ephemeral environments

### Deployment Strategies
- **Rolling Deployment** — Gradual replacement of old instances
- **Blue-Green Deployment** — Two environments, instant switchover
- **Canary Deployment** — Route small % of traffic to new version, monitor, expand
- **Feature Flags / Toggles** — Decouple deployment from release (LaunchDarkly, Unleash, Flagsmith)
- **A/B Testing** — Route users to different versions, measure outcomes
- **Dark Launches** — Deploy code without exposing to users, shadow traffic
- **Rollback** — Automated rollback on failure detection, database rollback challenges

### Release Engineering
- **Semantic Versioning (SemVer)** — MAJOR.MINOR.PATCH
- **Changelog** — Conventional commits, auto-generated changelogs
- **Release Trains** — Scheduled releases, cut branches at intervals
- **Hotfixes** — Emergency fixes, cherry-pick to release branch

---

## [[Methodologies]]

### Agile
- **Agile Manifesto** — Individuals/interactions, working software, customer collaboration, responding to change
- **Agile Principles** — Continuous delivery, welcome change, frequent delivery, sustainable pace
- **User Stories** — As a [user], I want [feature], so that [benefit]
- **Acceptance Criteria** — Given-When-Then, definition of done

### Scrum
- **Roles** — Product Owner, Scrum Master, Development Team
- **Ceremonies** — Sprint Planning, Daily Standup, Sprint Review, Sprint Retrospective
- **Artifacts** — Product Backlog, Sprint Backlog, Increment
- **Sprint** — Fixed time-box (usually 2 weeks), potentially shippable increment
- **Velocity** — Story points completed per sprint, forecasting

### Kanban
- **Core Concepts** — Visualize workflow, limit WIP (work in progress), manage flow
- **Kanban Board** — Columns for workflow stages, cards for work items
- **Metrics** — Cycle time, lead time, throughput, cumulative flow diagram
- **Pull System** — New work pulled when capacity is available

### Other Approaches
- **Extreme Programming (XP)** — Pair programming, TDD, continuous integration, simple design, refactoring
- **Shape Up (Basecamp)** — 6-week cycles, shaping, betting, cooldown
- **SAFe (Scaled Agile)** — Agile at enterprise scale (controversial)
- **Lean Software Development** — Eliminate waste, amplify learning, decide late, deliver fast

---

## [[Code Quality]]

### Code Review
- **Purpose** — Knowledge sharing, bug catching, consistency, mentoring
- **Best Practices** — Small PRs, clear descriptions, constructive feedback
- **Review Focus** — Logic correctness, edge cases, readability, security, performance
- **Approval Workflows** — Required reviewers, CODEOWNERS, auto-assign

### Static Analysis & Linting
- **Linters** — ESLint (JS), Pylint/Ruff (Python), RuboCop (Ruby), golangci-lint (Go)
- **Formatters** — Prettier, Black, gofmt, rustfmt
- **Static Analysis** — SonarQube, Semgrep, CodeClimate, SpotBugs
- **Type Checking** — TypeScript, mypy, Flow

### Refactoring
- **Code Smells** — Long methods, God classes, feature envy, primitive obsession, data clumps
- **Refactoring Techniques** — Extract method/class, rename, move, inline, introduce parameter object
- **Martin Fowler's Catalog** — Comprehensive reference for refactoring patterns
- **Refactoring Safety** — Tests as a safety net, small steps, continuous refactoring

### Technical Debt
- **Definition** — Implied cost of rework caused by choosing expedient solutions
- **Types** — Deliberate vs inadvertent, reckless vs prudent (Technical Debt Quadrant)
- **Managing Debt** — Track, prioritize, allocate capacity, pay down incrementally
- **Architecture Decision Records (ADRs)** — Document decisions and their rationale
- **Documentation** — README, API docs, architecture docs, runbooks (see [[Technical Communication]])

---

#process #git #testing #cicd #agile
