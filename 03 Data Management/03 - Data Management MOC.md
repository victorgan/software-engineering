# 03 — Data Management MOC

> ← Back to [[Software Engineering - Map of Content]]

Storing, retrieving, transforming, and moving data. Arguably the most critical concern in most applications — get this wrong and nothing else matters.

---

## [[Relational Databases]]

### SQL Fundamentals
- **DDL (Data Definition Language)** — CREATE, ALTER, DROP, TRUNCATE
- **DML (Data Manipulation Language)** — SELECT, INSERT, UPDATE, DELETE
- **Joins** — INNER, LEFT/RIGHT OUTER, FULL OUTER, CROSS, self-joins
- **Subqueries** — Correlated, non-correlated, EXISTS, IN
- **Aggregation** — GROUP BY, HAVING, window functions (ROW_NUMBER, RANK, LAG, LEAD, SUM OVER)
- **CTEs (Common Table Expressions)** — WITH clauses, recursive CTEs
- **Set Operations** — UNION, INTERSECT, EXCEPT

### Normalization
- **1NF** — Atomic values, no repeating groups
- **2NF** — No partial dependencies on composite keys
- **3NF** — No transitive dependencies
- **BCNF** — Every determinant is a candidate key
- **Denormalization** — Strategic redundancy for read performance (used in [[Data Modeling]])

### Indexing
- **B-Tree Indexes** — Default, good for range queries and equality
- **Hash Indexes** — O(1) equality lookups, no range support
- **Composite Indexes** — Multi-column, leftmost prefix rule
- **Covering Indexes** — Include all queried columns, avoid table lookups
- **Partial/Filtered Indexes** — Index a subset of rows
- **Full-Text Indexes** — Text search with ranking (tsvector in Postgres)
- **GIN/GiST Indexes** — JSONB, arrays, geometric data (Postgres)
- **Index Anti-Patterns** — Over-indexing, unused indexes, low selectivity

### Query Optimization
- **Query Plans** — EXPLAIN / EXPLAIN ANALYZE
- **Query Planner** — Cost-based optimization, statistics, cardinality estimation
- **Common Optimizations** — Index selection, join ordering, predicate pushdown
- **N+1 Query Problem** — Eager loading, batch loading, DataLoader pattern
- **Slow Query Analysis** — Query logs, pg_stat_statements, slow query logs

### Transactions & Concurrency
- **ACID Properties** — Atomicity, Consistency, Isolation, Durability
- **Isolation Levels** — Read Uncommitted, Read Committed, Repeatable Read, Serializable
- **Concurrency Phenomena** — Dirty reads, non-repeatable reads, phantom reads, write skew
- **Locking** — Row-level, table-level, advisory locks, deadlock detection
- **MVCC (Multi-Version Concurrency Control)** — Snapshot isolation, used in Postgres and MySQL InnoDB
- **Optimistic vs Pessimistic Locking** — Version columns vs SELECT FOR UPDATE
- **Two-Phase Commit (2PC)** — Distributed transactions (see [[Distributed Systems]])

### Major Relational Databases
- **PostgreSQL** — Open source, advanced features (JSONB, CTEs, window functions, extensions like PostGIS, pg_vector), strong SQL compliance, MVCC, extensible type system. The default choice for most new projects.
- **MySQL / MariaDB** — Open source, widely deployed (WordPress, many web apps), InnoDB engine, good replication story, simpler than Postgres. MariaDB is a community fork with additional features.
- **SQLite** — Open source, embedded, serverless, single-file, zero configuration. Ideal for mobile, desktop, edge, and testing. Not for concurrent write-heavy workloads.
- **SQL Server** — Commercial (Microsoft), T-SQL, strong BI/reporting tooling, tight Azure integration, enterprise features. Free tier: SQL Server Express.
- **Oracle Database** — Commercial, PL/SQL, RAC clustering, Exadata, mature enterprise features. Expensive licensing, strong in legacy enterprise environments.
- **CockroachDB** — Open source core, distributed SQL (Postgres-compatible wire protocol), serializable isolation by default, multi-region, auto-sharding.
- **YugabyteDB** — Open source, distributed SQL, Postgres-compatible, tunable consistency, multi-region.
- **AlloyDB** — Google Cloud managed Postgres-compatible, columnar engine for analytics, Postgres wire protocol.

### Partitioning (Single-Node)
- **Table Partitioning** — Split a large table into smaller physical pieces while presenting one logical table
- **Range Partitioning** — Partition by value range (e.g., date ranges, ID ranges). Good for time-series, archival. Risk: uneven partition sizes.
- **List Partitioning** — Partition by specific values (e.g., region = 'US', 'EU', 'APAC'). Good for geographic or categorical splits.
- **Hash Partitioning** — Partition by hash of a column. Even distribution, but range queries span all partitions.
- **Composite Partitioning** — Combine methods (e.g., range by year, then hash by user_id within each year)
- **Partition Pruning** — Query planner skips irrelevant partitions, major performance win for large tables
- **Postgres Partitioning** — Declarative partitioning (PARTITION BY RANGE/LIST/HASH), partition-wise joins, partition-wise aggregation
- **MySQL Partitioning** — Supports RANGE, LIST, HASH, KEY partitioning; less flexible than Postgres
- **When to Partition** — Tables exceeding tens of millions of rows, time-based data with retention policies, queries that naturally filter on the partition key

### Choosing a Relational Database — Tradeoffs
- **Open Source vs Commercial** — Postgres/MySQL are free, avoid vendor lock-in, large community. Oracle/SQL Server have dedicated support, enterprise tooling, but expensive licensing and lock-in.
- **Postgres vs MySQL** — Postgres: richer SQL features, better extensibility, stricter correctness, JSONB. MySQL: simpler operations, faster simple reads, wider hosting support, more forgiving defaults.
- **Single-Node vs Distributed SQL** — Single-node (Postgres, MySQL): simpler operations, mature tooling. Distributed SQL (CockroachDB, YugabyteDB): horizontal scale, multi-region, but more operational complexity and latency overhead.
- **Managed vs Self-Hosted** — Managed (RDS, Cloud SQL, Aurora): less ops burden, automated backups/patching, higher cost. Self-hosted: full control, lower cost at scale, but you own uptime.
- **Decision Factors** — Data model complexity, read/write ratio, transaction requirements, scale needs (vertical limit?), team expertise, ecosystem/tooling, licensing cost, cloud provider alignment, compliance requirements.

---

## [[NoSQL Databases]]

### Document Stores
- **Concept** — JSON/BSON documents, flexible schema, nested data
- **MongoDB** — Open source (SSPL license), collections, documents, aggregation pipeline, Atlas (managed). Most popular document DB, large ecosystem, sharding support.
- **CouchDB** — Open source (Apache), multi-master replication, eventual consistency, HTTP API
- **Amazon DocumentDB** — Managed, MongoDB-compatible API (not actual MongoDB engine)
- **Firestore** — Google Cloud managed, real-time sync, offline support, good for mobile/web apps
- **Use Cases** — Content management, user profiles, catalogs, event data, configuration
- **Tradeoffs** — Flexible schema speeds development but can lead to data inconsistency. No joins means denormalization and data duplication. Better for read-heavy, evolving schemas; worse for complex transactions.

### Key-Value Stores
- **Concept** — Simple get/set by key, extremely fast, minimal query capabilities
- **Redis** — Open source (BSD → SSPL), in-memory, data structures (lists, sets, sorted sets, streams), pub/sub, Lua scripting. Also used as cache, message broker, rate limiter.
- **Valkey** — Open source fork of Redis (Linux Foundation), community-driven after Redis license change
- **DynamoDB** — AWS managed, partition key + sort key, auto-scaling, single-digit ms latency, pay-per-request pricing
- **etcd** — Open source, distributed KV store, used in Kubernetes for coordination, Raft consensus
- **Memcached** — Open source, simple in-memory cache, multi-threaded, no persistence
- **Use Cases** — Session storage, [[Caching]], configuration, feature flags, leaderboards
- **Tradeoffs** — Fastest access patterns but limited query flexibility. Redis vs Memcached: Redis has richer data structures and persistence; Memcached is simpler, multi-threaded, and slightly faster for basic caching. DynamoDB: serverless and scalable but expensive at high throughput, vendor-locked.

### Column-Family Stores
- **Concept** — Wide columns, designed for write-heavy, time-series workloads, LSM-tree storage
- **Apache Cassandra** — Open source (Apache), distributed, tunable consistency, no single point of failure, linear scalability. Good for write-heavy workloads at massive scale.
- **HBase** — Open source (Apache), Hadoop ecosystem, strong consistency, good for random read/write on large datasets
- **ScyllaDB** — Open source core, C++ rewrite of Cassandra, lower tail latency, better hardware utilization
- **Google Bigtable** — Managed, inspired Cassandra/HBase, good for analytics and time-series at Google scale
- **Use Cases** — IoT data, event logs, time-series, messaging, recommendation data
- **Tradeoffs** — Excellent write throughput and horizontal scale, but poor for ad-hoc queries, joins, or transactions. Data modeling is query-driven (must know access patterns upfront). Operational complexity is high.

### Graph Databases
- **Concept** — Nodes, edges, and properties; optimized for relationship traversal
- **Neo4j** — Commercial + community edition, Cypher query language, native graph storage, ACID transactions
- **Amazon Neptune** — Managed, supports both Gremlin (property graph) and SPARQL (RDF)
- **ArangoDB** — Open source, multi-model (document + graph + key-value), AQL query language
- **Dgraph** — Open source, distributed graph DB, GraphQL-native
- **Use Cases** — Social networks, recommendation engines, knowledge graphs, fraud detection, access control
- **Tradeoffs** — Excels at traversing deep relationships (where relational joins would be expensive). Poor for bulk analytics, aggregations, or simple CRUD. Smaller ecosystem and tooling. Consider whether Postgres recursive CTEs or a relational model suffice before reaching for a graph DB.

### Time-Series Databases
- **Concept** — Optimized for timestamped data, compression, downsampling, retention policies
- **InfluxDB** — Open source, Flux/InfluxQL, retention policies, built for metrics and events
- **TimescaleDB** — Open source, PostgreSQL extension (full SQL support), hypertables, good when you want time-series + relational in one DB
- **Prometheus** — Open source, pull-based metrics collection, PromQL, designed for monitoring (see [[Observability]])
- **QuestDB** — Open source, high-performance ingestion, SQL interface
- **ClickHouse** — Open source, column-oriented OLAP database, extremely fast analytical queries, also strong for time-series
- **Use Cases** — Monitoring, IoT, financial data, sensor data, log analytics
- **Tradeoffs** — Fast ingestion and time-range queries, but limited general-purpose query capabilities. TimescaleDB wins when you need Postgres compatibility. ClickHouse wins for analytical queries. Prometheus is purpose-built for monitoring, not general time-series storage.

### Search Engines (as databases)
- **Elasticsearch** — Open source (SSPL), full-text search, inverted indexes, aggregations, ELK stack, distributed
- **OpenSearch** — Open source (Apache 2.0), AWS fork of Elasticsearch
- **Solr** — Open source (Apache), Lucene-based, mature, strong for faceted search
- **Typesense / Meilisearch** — Open source, modern developer-friendly alternatives, simpler to operate than Elasticsearch
- **Use Cases** — Full-text search, log analysis, product search, autocomplete, observability
- **Tradeoffs** — Best for text search and analytics, not a primary data store. Elasticsearch is powerful but operationally heavy (JVM tuning, cluster management). Typesense/Meilisearch are simpler but less featureful at scale.

---

## [[Database Selection Guide]]

### Key Decision Factors
- **Data Model** — Relational (structured, joins, transactions) vs document (flexible, nested) vs graph (relationships) vs time-series (temporal) vs key-value (simple lookups)
- **Read vs Write Ratio** — Read-heavy → Postgres + read replicas, caching. Write-heavy → Cassandra, DynamoDB, ClickHouse.
- **Consistency Requirements** — Strong consistency (financial, inventory) → Postgres, CockroachDB. Eventual consistency acceptable (social feeds, analytics) → Cassandra, DynamoDB, MongoDB.
- **Scale** — Vertical scaling sufficient (<10TB, <100K QPS) → Postgres/MySQL. Horizontal scaling needed → DynamoDB, Cassandra, CockroachDB, Vitess (MySQL sharding).
- **Query Complexity** — Complex joins, aggregations, ad-hoc queries → Relational. Known access patterns, denormalized → NoSQL. Full-text search → Elasticsearch/Typesense.
- **Latency Requirements** — Sub-millisecond → Redis/Memcached (in-memory). Single-digit ms → DynamoDB. Low ms → Postgres with proper indexing.
- **Operational Complexity** — Team size and expertise. Managed services (RDS, DynamoDB, Atlas) reduce burden. Self-hosted gives control but requires expertise.
- **Cost** — Open source: free but self-hosting costs. Managed: pay for convenience. Commercial licenses (Oracle, SQL Server): significant at scale. Serverless (DynamoDB, Firestore): pay-per-request, can be expensive at high throughput.
- **Ecosystem & Tooling** — ORMs, migration tools, monitoring, backup solutions, community support, hiring pool.
- **Vendor Lock-In** — Postgres, MySQL, Redis are portable. DynamoDB, Firestore, Cosmos DB are cloud-specific. Consider multi-cloud requirements.

### Common Combinations (Polyglot Persistence)
- **Web App** — Postgres (primary) + Redis (cache/sessions) + Elasticsearch (search)
- **IoT Platform** — TimescaleDB or InfluxDB (time-series) + Postgres (metadata) + Kafka (ingestion)
- **Social Platform** — Postgres or MySQL (users, posts) + Redis (feeds, caching) + Neo4j or Postgres (social graph) + Elasticsearch (search)
- **E-Commerce** — Postgres (orders, inventory) + Redis (cart, sessions) + Elasticsearch (product search) + ClickHouse (analytics)
- **Analytics Platform** — ClickHouse or BigQuery (OLAP) + Postgres (metadata) + Kafka (ingestion) + S3 (data lake)

---

## [[Sharding and Partitioning]]

*Partitioning splits data within a single database instance. Sharding distributes data across multiple database instances. Both reduce per-node data size; sharding also distributes load. See [[Distributed Systems]] for the theoretical foundations (CAP, consistency models, consensus).*

### Sharding Strategies
- **Range-Based Sharding** — Assign key ranges to shards (e.g., users A-M → shard 1, N-Z → shard 2). Simple to understand. Risk: hotspots if access is uneven (e.g., new users cluster in one range).
- **Hash-Based Sharding** — Hash the shard key, mod by shard count. Even distribution. Downside: range queries must hit all shards (scatter-gather).
- **Consistent Hashing** — Minimizes data movement when adding/removing shards. Used by DynamoDB, Cassandra, Riak. Virtual nodes improve balance.
- **Directory-Based Sharding** — A lookup table maps keys to shards. Maximum flexibility but the directory is a single point of failure and bottleneck.
- **Geographic Sharding** — Shard by region to keep data close to users. Reduces latency, aids data residency compliance (GDPR). Complicates global queries.

### Choosing a Shard Key
- **High Cardinality** — Key should have many distinct values to distribute evenly (user_id good, country bad)
- **Even Distribution** — Avoid keys that create hotspots (e.g., timestamp as shard key → all writes hit latest shard)
- **Query Alignment** — Most queries should include the shard key to avoid scatter-gather across all shards
- **Immutability** — Shard key should rarely change; changing it means moving data between shards
- **Compound Shard Keys** — Combine fields (e.g., tenant_id + user_id) for multi-tenant systems

### Sharding Challenges
- **Cross-Shard Queries** — Joins across shards are expensive or impossible; requires scatter-gather or denormalization
- **Cross-Shard Transactions** — ACID across shards requires 2PC or saga pattern; most sharded systems avoid this (see [[Distributed Systems]])
- **Rebalancing** — Adding shards requires data migration; consistent hashing minimizes movement, but it's still operationally complex
- **Hotspots** — Uneven access patterns concentrate load on specific shards; monitor and split hot shards
- **Operational Complexity** — Schema changes across shards, backup coordination, monitoring per-shard health
- **Referential Integrity** — Foreign keys can't span shards; enforce at application level or colocate related data

### Sharding Tools & Approaches
- **Application-Level Sharding** — Application code decides which shard to query. Full control but couples business logic to data distribution.
- **Vitess** — MySQL sharding middleware (created at YouTube/Google). Transparent sharding, connection pooling, online schema changes. Powers YouTube, Slack, Square.
- **Citus** — Postgres extension for distributed tables. Colocated joins, distributed queries, reference tables. Now part of Azure Cosmos DB for PostgreSQL.
- **ProxySQL / MaxScale** — MySQL proxies that can route queries to shards based on rules
- **Native Distributed Databases** — CockroachDB, YugabyteDB, Cloud Spanner, TiDB — handle sharding internally with automatic rebalancing. Trade: simpler operations but less control and some latency overhead.

### Sharding vs Alternatives
- **Vertical Scaling First** — Modern hardware (64+ cores, TBs of RAM, NVMe SSDs) handles more than most assume. Postgres on large instance handles millions of rows. Don't shard until you must.
- **Read Replicas** — If reads are the bottleneck, replicas may be enough without sharding (see Replication below)
- **Partitioning** — If data is large but queries are naturally scoped (by time, tenant), table partitioning within one instance may suffice
- **Caching Layer** — If read latency is the issue, a cache (Redis, Memcached) in front of the DB may eliminate the need to shard (see [[Caching]])
- **Archive Old Data** — If table size is the problem but most queries hit recent data, archive old rows to cold storage

### Replication (for Data Management)
- **Read Replicas** — Copies of the primary that serve reads. Offload read traffic. Replication lag means stale reads.
- **Synchronous vs Asynchronous Replication** — Sync: no data loss on failover, higher write latency. Async: low latency, but risk of data loss on failover.
- **Streaming Replication (Postgres)** — WAL-based, continuous, configurable sync/async
- **MySQL Replication** — Binary log (binlog) replication, GTID-based for consistency
- **Multi-Primary / Multi-Master** — Multiple writable nodes. Requires conflict resolution (last-writer-wins, CRDTs, application-level). Used in Galera Cluster, Aurora Multi-Master.
- **Logical Replication** — Replicate specific tables/rows, cross-version, cross-platform (Postgres logical replication, Debezium CDC)

---

## [[Data Modeling]]

### Conceptual Modeling
- **ER Diagrams** — Entities, relationships, cardinality (1:1, 1:N, N:M)
- **Conceptual vs Logical vs Physical Models** — Abstraction levels

### Relational Modeling
- **Normalization** — Eliminating redundancy (see Relational Databases above)
- **Denormalization** — Pre-joining for read performance
- **Schema Design Patterns** — Star schema, snowflake schema (for data warehousing)
- **Migrations** — Schema evolution, forward-only, reversible, zero-downtime migrations
- **Migration Tools** — Flyway, Liquibase, Alembic, ActiveRecord Migrations, Prisma

### NoSQL Modeling
- **Document Modeling** — Embedding vs referencing, polymorphic patterns
- **Access Pattern-Driven Design** — Design schema around queries, not entities
- **Single Table Design** — DynamoDB pattern, overloaded GSIs
- **Event Sourcing** — Store events as the source of truth, derive current state (see [[Architectural Patterns]])

---

## [[Caching]]

### Caching Strategies
- **Cache-Aside (Lazy Loading)** — App checks cache, fetches from DB on miss, writes to cache
- **Write-Through** — Write to cache and DB simultaneously
- **Write-Behind (Write-Back)** — Write to cache, async write to DB
- **Read-Through** — Cache itself fetches from DB on miss
- **Refresh-Ahead** — Proactively refresh before expiry

### Cache Invalidation
- **TTL (Time to Live)** — Expiry-based, simple but stale data risk
- **Event-Based Invalidation** — Invalidate on write events
- **Cache Stampede / Thundering Herd** — Locking, request coalescing, probabilistic early expiry
- **The Two Hard Problems** — "Cache invalidation and naming things"

### Caching Layers
- **Application-Level** — In-memory (Guava, Caffeine), local process cache
- **Distributed Cache** — Redis, Memcached, Hazelcast
- **CDN Caching** — Static assets, edge caching, cache-control headers (see [[Networking]])
- **Database Query Cache** — Query result caching, materialized views
- **HTTP Caching** — ETag, Last-Modified, Cache-Control, conditional requests
- **Browser Caching** — Service workers, localStorage (frontend-specific)

---

## [[Data Pipelines]]

### ETL vs ELT
- **ETL (Extract, Transform, Load)** — Transform before loading, traditional data warehousing
- **ELT (Extract, Load, Transform)** — Load raw data, transform in-place (modern approach with cheap storage)

### Batch Processing
- **Apache Hadoop** — MapReduce, HDFS, YARN
- **Apache Spark** — In-memory processing, RDDs, DataFrames, SparkSQL
- **dbt (data build tool)** — SQL-first transforms, version-controlled analytics
- **Airflow** — DAG-based workflow orchestration, scheduling

### Stream Processing
- **Apache Kafka** — Distributed log, topics, partitions, consumer groups, exactly-once semantics
- **Apache Flink** — Stateful stream processing, event time, watermarks
- **Apache Pulsar** — Multi-tenancy, tiered storage
- **Kafka Streams / ksqlDB** — Stream processing as a library / SQL on streams
- **Event-Driven Architecture** — Events as first-class citizens, CQRS, event sourcing (see [[Architectural Patterns]])

### Data Storage Tiers
- **Data Lake** — Raw, unstructured storage (S3, ADLS, GCS)
- **Data Lakehouse** — Combines lake + warehouse (Delta Lake, Apache Iceberg, Apache Hudi)
- **Data Warehouse** — Structured, optimized for analytics (Snowflake, BigQuery, Redshift, Databricks)
- **Data Mart** — Subset of warehouse for specific business domain

### Data Governance & Quality
- **Data Catalogs** — Metadata management, discovery (Amundsen, DataHub, Atlan)
- **Data Lineage** — Tracking data flow from source to consumption
- **Data Quality** — Validation, profiling, Great Expectations, dbt tests
- **Data Contracts** — Schema agreements between producers and consumers
- **PII & Compliance** — GDPR, CCPA, data masking, anonymization (see [[Infrastructure Security]])

### Change Data Capture (CDC)
- **Log-Based CDC** — Read database transaction logs (Debezium, Maxwell)
- **Trigger-Based CDC** — Database triggers on changes
- **Polling-Based CDC** — Periodic queries for changes
- **Use Cases** — Real-time sync, cache invalidation, event sourcing

---

#data #databases #caching #pipelines #database-selection #sharding #partitioning #replication
