# MillWheel to Dataflow Mapping

> <- Back to [[Data Systems Mapping]]

| | Google Internal | Open Source | GCP |
|---|---|---|---|
| System | MillWheel | Apache Beam (streaming) | Dataflow |
| Concept | Stream processing | Stream processing | Managed stream processing |

MillWheel (2013 paper) was Google's stream processing framework with exactly-once semantics and low latency. Its concepts heavily influenced Apache Beam's streaming model and the Dataflow service on GCP. Key contributions: watermarks, windowing, and exactly-once processing guarantees.

---

#google-internal #mapping #millwheel #dataflow
