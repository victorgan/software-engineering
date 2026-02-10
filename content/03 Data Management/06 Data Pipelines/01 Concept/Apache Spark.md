# Apache Spark

> <- Back to [[Batch Processing]]

Open source unified analytics engine with in-memory processing. Core abstractions: RDDs, DataFrames, and SparkSQL. Significantly faster than Hadoop MapReduce for iterative workloads due to in-memory DAG execution.

## Key Properties

- [[In-Memory Processing]]
- [[RDDs]]
- [[DataFrames]]
- [[SparkSQL]]

## How It Works

Builds a DAG (directed acyclic graph) of transformations that are lazily evaluated and optimized before execution. Data is kept in memory between stages rather than written to disk, making iterative algorithms (ML, graph) orders of magnitude faster than MapReduce. Catalyst optimizer handles query planning for DataFrames and SparkSQL.

## Ecosystem

- **Spark SQL** — structured data queries via DataFrames and SQL
- **Spark Streaming / Structured Streaming** — micro-batch and continuous stream processing
- **MLlib** — distributed machine learning library
- **GraphX** — graph computation

## Related

- [[Apache Hadoop]] (predecessor, disk-based MapReduce)
- [[Apache Beam]] (portable abstraction that can run on Spark)
- [[Apache Flink]] (alternative with native streaming)
- [[Trino]] (SQL query engine, complementary for interactive queries)

---

#data-pipelines #batch #spark
