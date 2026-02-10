# Trino

> <- Back to [[Batch Processing]]

Open source distributed SQL query engine (formerly PrestoSQL, originated at Facebook) for interactive analytics across heterogeneous data sources. Queries data in place without requiring ETL into a separate system — a single SQL query can join across a data lake, a relational database, and a key-value store.

## Key Properties

- [[Federated Queries]]
- [[Connector Architecture]]
- [[MPP (Massively Parallel Processing)]]
- [[Query Optimization]]

## How It Works

A coordinator node parses SQL, plans the query, and distributes work across worker nodes. Connectors abstract data sources (Hive/S3, PostgreSQL, Kafka, Elasticsearch, etc.) behind a common interface. Executes entirely in memory with pipelined stages — no intermediate disk writes — optimized for low-latency interactive queries rather than long-running ETL.

## Connectors

- **Hive / S3** — query Parquet, ORC, Avro files in data lakes
- **Iceberg / Delta Lake** — table formats with ACID semantics
- **RDBMS** — PostgreSQL, MySQL, SQL Server
- **NoSQL** — Cassandra, Elasticsearch, MongoDB, Redis

## Related

- [[Data Lakehouse]] (Trino commonly used as the query layer)
- [[Data Warehouse]] (alternative approach — Trino queries data in place instead)
- [[Apache Spark]] (complementary — Spark for heavy ETL, Trino for interactive queries)
- [[BigQuery]] (managed alternative on GCP)

---

#data-pipelines #batch #trino
