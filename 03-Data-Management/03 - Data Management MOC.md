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
- **PostgreSQL** — Advanced features, JSONB, extensions, strong SQL compliance
- **MySQL / MariaDB** — Widely deployed, InnoDB engine, replication
- **SQLite** — Embedded, serverless, single-file, used in mobile/desktop
- **SQL Server** — Enterprise, T-SQL, strong tooling
- **Oracle** — Enterprise, PL/SQL, RAC clustering

---

## [[NoSQL Databases]]

### Document Stores
- **Concept** — JSON/BSON documents, flexible schema, nested data
- **MongoDB** — Collections, documents, aggregation pipeline, Atlas
- **CouchDB** — Multi-master replication, eventual consistency
- **Use Cases** — Content management, user profiles, catalogs

### Key-Value Stores
- **Concept** — Simple get/set by key, extremely fast
- **Redis** — In-memory, data structures (lists, sets, sorted sets, streams), pub/sub
- **DynamoDB** — AWS managed, partition key + sort key, auto-scaling
- **etcd** — Distributed KV store, used in Kubernetes for coordination
- **Use Cases** — Session storage, [[Caching]], configuration, feature flags

### Column-Family Stores
- **Concept** — Wide columns, designed for write-heavy, time-series workloads
- **Apache Cassandra** — Distributed, tunable consistency, no single point of failure
- **HBase** — Hadoop ecosystem, strong consistency
- **ScyllaDB** — C++ rewrite of Cassandra, lower latency
- **Use Cases** — IoT data, event logs, time-series, messaging

### Graph Databases
- **Concept** — Nodes, edges, and properties; optimized for relationship traversal
- **Neo4j** — Cypher query language, native graph storage
- **Amazon Neptune** — Managed graph DB, Gremlin + SPARQL
- **Use Cases** — Social networks, recommendation engines, knowledge graphs, fraud detection

### Time-Series Databases
- **Concept** — Optimized for timestamped data, compression, downsampling
- **InfluxDB** — Flux query language, retention policies
- **TimescaleDB** — PostgreSQL extension, hypertables
- **Prometheus** — Pull-based metrics collection (see [[Observability]])
- **Use Cases** — Monitoring, IoT, financial data, sensor data

### Search Engines (as databases)
- **Elasticsearch** — Full-text search, inverted indexes, aggregations, ELK stack
- **OpenSearch** — AWS fork of Elasticsearch
- **Solr** — Apache, Lucene-based
- **Typesense / Meilisearch** — Modern, developer-friendly alternatives
- **Use Cases** — Full-text search, log analysis, product search, autocomplete

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

#data #databases #caching #pipelines
