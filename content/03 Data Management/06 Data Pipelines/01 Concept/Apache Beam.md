# Apache Beam

> <- Back to [[Batch Processing]]

Open source unified programming model for batch and stream data processing. Defines pipelines that are portable across execution engines (runners) like Google Cloud Dataflow, Apache Flink, and Apache Spark. Originated from Google's internal FlumeJava and MillWheel systems.

## Key Properties

- [[Unified Batch and Stream Model]]
- [[Pipeline Runners]]
- [[Windowing]]
- [[Watermarks]]

## How It Works

Pipelines are defined as a DAG of PTransforms (parallel transforms) applied to PCollections (distributed datasets). The same pipeline code runs on any supported runner — the Beam SDK translates the logical plan into the runner's native execution. Windowing and triggers control how unbounded (streaming) data is grouped and emitted.

## Runners

- **Google Cloud Dataflow** — fully managed, autoscaling (the reference runner)
- **Apache Flink** — low-latency streaming
- **Apache Spark** — batch-oriented workloads
- **Direct Runner** — local testing and development

## Related

- [[Apache Spark]] (can serve as a Beam runner)
- [[Apache Flink]] (can serve as a Beam runner)
- [[FlumeJava to Beam Mapping]] (Google internal lineage)
- [[Watermarks]] (shared concept with Flink for event-time processing)

---

#data-pipelines #batch #streaming #beam
