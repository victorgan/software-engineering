# Dapper to Zipkin Mapping

> <- Back to [[Operations and Security Mapping]]

| | Google Internal | Open Source | GCP |
|---|---|---|---|
| System | Dapper | Zipkin, Jaeger, OpenTelemetry | Cloud Trace |
| Concept | Distributed tracing | Distributed tracing | Managed tracing |

Dapper (2010 paper) is Google's distributed tracing infrastructure. Zipkin (by Twitter) and Jaeger (by Uber) were directly inspired by the Dapper paper. OpenTelemetry unifies tracing standards across the industry. Cloud Trace is the managed GCP service. All share Dapper's fundamental concepts: trace IDs, spans, and parent-child relationships.

---

#google-internal #mapping #dapper #zipkin
