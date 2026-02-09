# 05 — Software Design & Architecture MOC

> ← Back to [[Software Engineering - Map of Content]]

How you structure code and systems. Good design is what allows software to evolve over years without collapsing under its own weight.

---

## [[OOP and SOLID Principles]]

### Core OOP Concepts
- **Encapsulation** — Hide internal state, expose behavior through interfaces
- **Abstraction** — Modeling real concepts, hiding complexity
- **Inheritance** — Reuse through parent-child relationships, "is-a"
- **Polymorphism** — Same interface, different implementations
- **Composition vs Inheritance** — "Has-a" vs "is-a", favor composition for flexibility

### SOLID Principles
- **S — Single Responsibility** — A class should have one reason to change
- **O — Open/Closed** — Open for extension, closed for modification
- **L — Liskov Substitution** — Subtypes must be substitutable for their base types
- **I — Interface Segregation** — Many specific interfaces over one general interface
- **D — Dependency Inversion** — Depend on abstractions, not concretions

### Other Design Principles
- **DRY (Don't Repeat Yourself)** — Single source of truth for every piece of knowledge
- **KISS (Keep It Simple, Stupid)** — Simplest solution that works
- **YAGNI (You Ain't Gonna Need It)** — Don't build features speculatively
- **Law of Demeter** — Only talk to your immediate friends (minimize coupling)
- **Tell, Don't Ask** — Command objects, don't interrogate them
- **Separation of Concerns** — Each module addresses a distinct concern
- **Principle of Least Astonishment** — Code should do what the reader expects

---

## [[Design Patterns]]

### Creational Patterns
- **Singleton** — One instance globally (controversy: hidden global state)
- **Factory Method** — Delegate instantiation to subclasses
- **Abstract Factory** — Family of related objects without specifying classes
- **Builder** — Step-by-step construction of complex objects
- **Prototype** — Clone existing objects

### Structural Patterns
- **Adapter** — Convert one interface to another
- **Decorator** — Add behavior dynamically without modifying class
- **Facade** — Simplified interface to a complex subsystem
- **Proxy** — Placeholder that controls access (lazy loading, caching, auth)
- **Composite** — Tree structures, treat individual and composite uniformly
- **Bridge** — Decouple abstraction from implementation
- **Flyweight** — Share common state to reduce memory

### Behavioral Patterns
- **Observer** — Pub/sub within an application, event notification
- **Strategy** — Interchangeable algorithms, runtime selection
- **Command** — Encapsulate requests as objects, undo/redo
- **State** — Object behavior changes based on internal state
- **Template Method** — Define algorithm skeleton, let subclasses fill steps
- **Iterator** — Sequential access to collection elements
- **Chain of Responsibility** — Pass requests along a chain of handlers (middleware)
- **Mediator** — Centralize complex communications between objects
- **Visitor** — Add operations to object structures without modifying them
- **Memento** — Capture and restore object state (undo/redo)

### Modern / Functional Patterns
- **Dependency Injection** — Provide dependencies externally, inversion of control
- **Repository Pattern** — Abstract data access behind a collection-like interface
- **Unit of Work** — Track changes, commit atomically
- **Specification Pattern** — Composable business rules
- **Middleware / Pipeline** — Chain of processing steps (Express.js, Django, ASP.NET)
- **Result/Option Types** — Error handling without exceptions (Rust Result, Haskell Maybe)
- **Monad Pattern** — Composable computation chains (see [[Programming Paradigms|Functional Programming]])

---

## [[Architectural Patterns]]

### Monolith
- **Modular Monolith** — Well-structured monolith with clear module boundaries
- **When to Use** — Early-stage products, small teams, low complexity
- **Strangler Fig** — Incrementally migrate monolith to microservices

### Microservices
- **Principles** — Single responsibility per service, independent deployment, own data store
- **Inter-Service Communication** — Sync (HTTP/gRPC) vs Async (message queues, events)
- **Service Discovery** — DNS-based, registry (Consul, Eureka), K8s services
- **Data Ownership** — Each service owns its data, no shared databases
- **Challenges** — Distributed transactions, debugging, operational complexity, data consistency
- **Saga Pattern** — Choreography (events) or Orchestration (central coordinator)

### Event-Driven Architecture
- **Event Sourcing** — Store events, derive state, complete audit trail
- **CQRS (Command Query Responsibility Segregation)** — Separate read and write models
- **Event Bus / Broker** — Kafka, RabbitMQ, EventBridge
- **Domain Events** — Meaningful business events, loose coupling between bounded contexts
- **Event Storming** — Collaborative design workshop technique

### Layered Architecture
- **Classic Layers** — Presentation → Business Logic → Data Access → Database
- **Clean Architecture** — Entities → Use Cases → Interface Adapters → Frameworks (Uncle Bob)
- **Hexagonal Architecture (Ports & Adapters)** — Core domain isolated from infrastructure
- **Onion Architecture** — Similar to hexagonal, concentric layers of dependency

### Other Architectural Styles
- **Serverless Architecture** — FaaS + managed services, event-driven (see [[Cloud and Containers]])
- **Space-Based Architecture** — In-memory data grids, processing units (for extreme scale)
- **Pipe and Filter** — Data flows through processing stages (Unix philosophy)
- **Plugin Architecture** — Core + extensible plugins (IDEs, browsers, WordPress)
- **Micro-Frontends** — Independent frontend modules, composed at runtime or build time

---

## [[API Design]]

### REST
- **Resource-Oriented** — URLs represent resources, HTTP methods as operations
- **Richardson Maturity Model** — Level 0 (RPC) → Level 3 (HATEOAS)
- **Best Practices** — Plural nouns, proper status codes, pagination, filtering, sorting
- **Pagination** — Offset-based, cursor-based, keyset pagination
- **Versioning** — URL path (/v1/), header-based, query parameter
- **HATEOAS** — Hypermedia links in responses (rarely fully implemented)

### GraphQL
- **Core Concepts** — Schema, queries, mutations, subscriptions, resolvers
- **Type System** — Scalar, Object, Enum, Interface, Union, Input
- **Advantages** — Client-specified data, single endpoint, strong typing
- **Challenges** — N+1 queries (DataLoader), complexity limiting, caching
- **Federation** — Distributed graph across services (Apollo Federation)

### gRPC
- **Protocol Buffers (protobuf)** — Binary serialization, schema definition (.proto files)
- **Communication Patterns** — Unary, server streaming, client streaming, bidirectional streaming
- **Advantages** — High performance, strong typing, code generation, HTTP/2
- **Use Cases** — Service-to-service communication, low-latency, polyglot environments

### API Best Practices
- **Idempotency** — Safe to retry (idempotency keys)
- **Rate Limiting** — Token bucket, sliding window, leaky bucket
- **Authentication** — API keys, OAuth 2.0, JWT (see [[Authentication and Authorization]])
- **Documentation** — OpenAPI/Swagger, API Blueprint, Postman
- **Backward Compatibility** — Additive changes, deprecation policy
- **Error Handling** — Consistent error format, error codes, problem details (RFC 7807)
- **SDK Generation** — Auto-generate client libraries from spec

---

## [[Domain-Driven Design]]

### Strategic Design
- **Bounded Contexts** — Explicit boundary where a model applies
- **Ubiquitous Language** — Shared vocabulary between developers and domain experts
- **Context Mapping** — Relationships between bounded contexts (shared kernel, customer-supplier, conformist, anti-corruption layer)
- **Subdomains** — Core (competitive advantage), Supporting (necessary), Generic (commodity)

### Tactical Design
- **Entities** — Objects defined by identity (not attributes)
- **Value Objects** — Defined by attributes, immutable, no identity
- **Aggregates** — Cluster of entities/value objects with a root entity, consistency boundary
- **Domain Events** — Record of something significant that happened
- **Repositories** — Abstract persistence of aggregates
- **Domain Services** — Stateless operations that don't belong to an entity
- **Factories** — Complex object creation encapsulated
- **Application Services** — Orchestrate use cases, coordinate domain objects

### DDD in Practice
- **Event Storming** — Workshop to discover domain events, commands, aggregates
- **Specification Pattern** — Express business rules as objects
- **Anti-Corruption Layer** — Translate between models at context boundaries
- **CQRS with DDD** — Separate command and query models aligned with aggregates

---

## [[System Design Tradeoffs]]

### Fundamental Tradeoffs
- **Consistency vs Availability** — CAP theorem in practice; strong consistency costs availability under partition (see [[Distributed Systems]])
- **Latency vs Throughput** — Batching improves throughput but increases per-request latency
- **Simplicity vs Flexibility** — Generic systems handle more cases but are harder to understand and maintain
- **Read vs Write Optimization** — Denormalization and caching speed reads at the cost of write complexity (see [[Data Modeling]])
- **Cost vs Performance** — More resources improve performance with diminishing returns; serverless vs provisioned
- **Coupling vs Autonomy** — Monoliths are coupled but consistent; microservices are autonomous but operationally complex

### When to Choose What

#### Monolith vs Microservices
- **Choose Monolith** — Small team (<10 engineers), early-stage product, unclear domain boundaries, need to ship fast
- **Choose Microservices** — Large org with multiple teams, well-understood domain, independent scaling needs, polyglot requirements
- **Modular Monolith** — Best of both: monolith deployment, clean module boundaries, easy to split later

#### SQL vs NoSQL
- **Choose SQL** — Complex queries, joins, transactions, data integrity is critical, ad-hoc reporting (see [[Database Selection Guide]])
- **Choose NoSQL** — Known access patterns, high write throughput, flexible schema, horizontal scaling, denormalized data

#### REST vs GraphQL vs gRPC
- **Choose REST** — Public APIs, broad client support, simple CRUD, caching matters (HTTP caching)
- **Choose GraphQL** — Multiple client types (mobile, web) with different data needs, nested data, rapid frontend iteration
- **Choose gRPC** — Service-to-service, low latency, streaming, strong typing, polyglot backend services

#### Sync vs Async Communication
- **Choose Sync (HTTP/gRPC)** — Low latency needed, simple request-response, strong consistency requirement
- **Choose Async (Queues/Events)** — Decoupled services, eventual consistency acceptable, spike traffic handling, long-running tasks

#### Build vs Buy
- **Build** — Core competency, unique differentiator, no good existing solution, control is critical
- **Buy/Use OSS** — Commodity problem, well-served by existing tools, team doesn't have domain expertise, speed to market

### Design Review Checklist
- **Scalability** — What happens at 10x, 100x current load? Where are the bottlenecks?
- **Failure Modes** — What happens when each dependency fails? Is there graceful degradation? (see [[Reliability Patterns]])
- **Data Consistency** — What consistency model is needed? What happens during network partition?
- **Security** — What are the trust boundaries? How is auth handled? What data is sensitive? (see [[Application Security]])
- **Observability** — How will you know it's working? What metrics, logs, traces? (see [[Observability]])
- **Operability** — How is it deployed? Can it be rolled back? What does on-call look like? (see [[Site Reliability Engineering]])
- **Cost** — What are the infrastructure costs? How does cost scale with usage?
- **Migration** — How do you get from current state to proposed state without downtime?

---

#design #architecture #patterns #api #tradeoffs
