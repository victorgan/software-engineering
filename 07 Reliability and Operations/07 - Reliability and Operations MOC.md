# 07 — Reliability & Operations MOC

> ← Back to [[Software Engineering - Map of Content]]

Keeping systems running, performant, and recoverable. The difference between a demo and production is reliability.

---

## [[Observability]]

### The Three Pillars
- **Logs** — Discrete events with context, structured (JSON) vs unstructured
- **Metrics** — Numeric measurements over time (counters, gauges, histograms)
- **Traces** — End-to-end request path through distributed services

### Logging
- **Structured Logging** — Key-value pairs, JSON format, machine-parseable
- **Log Levels** — DEBUG, INFO, WARN, ERROR, FATAL
- **Correlation IDs / Request IDs** — Trace a request across services
- **Log Aggregation** — ELK Stack (Elasticsearch, Logstash, Kibana), Loki + Grafana, Splunk, Datadog
- **Sampling** — Log a percentage to manage volume at scale
- **Best Practices** — Don't log PII, include context, structured over printf

### Metrics
- **Metric Types** — Counter (monotonically increasing), Gauge (current value), Histogram (distribution), Summary
- **RED Method** — Rate, Errors, Duration (for request-driven services)
- **USE Method** — Utilization, Saturation, Errors (for resources: CPU, memory, disk, network)
- **Four Golden Signals (Google SRE)** — Latency, Traffic, Errors, Saturation
- **Tools** — Prometheus, Grafana, Datadog, CloudWatch, StatsD, InfluxDB
- **Percentiles** — p50, p95, p99, p99.9 — more informative than averages

### Distributed Tracing
- **Concepts** — Spans, traces, parent-child relationships, baggage/context propagation
- **OpenTelemetry** — Vendor-neutral standard for traces, metrics, and logs
- **Jaeger** — Open-source distributed tracing
- **Zipkin** — Another open-source tracing system
- **AWS X-Ray, Datadog APM** — Managed tracing solutions
- **Trace Sampling** — Head-based vs tail-based sampling

### Dashboards & Alerting
- **Dashboard Design** — Hierarchy of information, actionable views, not vanity metrics
- **Grafana** — Open-source dashboarding, data source agnostic
- **Alerting Philosophy** — Alert on symptoms not causes, reduce noise, actionable alerts
- **Alert Fatigue** — Too many alerts → ignored alerts → incidents
- **PagerDuty / OpsGenie / Incident.io** — Alert routing, escalation, on-call management

---

## [[Incident Management]]

### On-Call
- **On-Call Rotations** — Primary/secondary, follow-the-sun, fair scheduling
- **Runbooks** — Step-by-step guides for common incidents
- **Escalation Policies** — When and how to escalate
- **Toil** — Repetitive operational work that should be automated

### Incident Response
- **Severity Levels** — SEV1 (critical) through SEV4 (minor)
- **Incident Commander** — Central coordination role during incidents
- **Communication** — Status pages, internal updates, customer communication
- **Mitigation vs Root Cause Fix** — Stop the bleeding first, fix properly later
- **War Rooms** — Real-time coordination (Slack channels, video calls)

### Post-Incident Process
- **Blameless Post-Mortems** — Focus on systems and processes, not individuals
- **Post-Mortem Template** — Summary, timeline, impact, root cause, contributing factors, action items
- **5 Whys** — Root cause analysis technique
- **Action Items** — Concrete, assigned, tracked, prioritized
- **Learning Culture** — Share post-mortems widely, celebrate learning from failure

---

## [[Site Reliability Engineering]]

### SLAs, SLOs, SLIs
- **SLI (Service Level Indicator)** — Measurable metric (e.g., latency p99 < 200ms)
- **SLO (Service Level Objective)** — Target for an SLI (e.g., 99.9% of requests < 200ms)
- **SLA (Service Level Agreement)** — Contractual commitment with consequences
- **Choosing SLOs** — Based on user expectations, not technical capability
- **The Nines** — 99.9% = 8.76h downtime/year, 99.99% = 52.6min/year

### Error Budgets
- **Concept** — Allowed unreliability = 1 - SLO target
- **Budget Consumption** — Track error budget burn rate
- **Budget Policy** — When budget is exhausted → focus on reliability over features
- **Burn Rate Alerts** — Alert when burning budget too fast

### Toil Management
- **Definition** — Manual, repetitive, automatable, tactical, no enduring value
- **Toil Budget** — SRE teams aim for < 50% toil
- **Automation** — Self-healing systems, auto-remediation, infrastructure as code
- **Elimination Strategies** — Automate, simplify, eliminate the need

### Reliability Patterns
- **Graceful Degradation** — Reduced functionality instead of total failure
- **Circuit Breakers** — Stop calling failing services (see [[Distributed Systems]])
- **Bulkheads** — Isolate failures to prevent cascading
- **Timeouts** — Always set timeouts, use adaptive timeouts
- **Retries** — Exponential backoff with jitter, idempotency requirement
- **Rate Limiting** — Protect services from overload (see [[API Design]])
- **Health Checks** — Liveness probes, readiness probes, startup probes
- **Redundancy** — No single points of failure, multi-AZ, multi-region

### SRE Team Models
- **Embedded SRE** — SREs sit within product teams, deep product context
- **Centralized / Platform SRE** — Shared SRE team provides tools and platforms for all teams
- **Consulting SRE** — SREs advise teams on reliability, teams own their services
- **SRE vs DevOps** — SRE is a specific implementation of DevOps principles with prescriptive practices
- **Service Ownership** — "You build it, you run it" — teams own production behavior of their services
- **Production Readiness Reviews (PRR)** — Checklist before a new service goes to production (monitoring, alerting, runbooks, load testing, failover)

---

## [[Disaster Recovery & Business Continuity]]

### Backup & Restore
- **Backup Strategies** — Full, incremental, differential backups
- **RPO (Recovery Point Objective)** — Maximum acceptable data loss (time-based)
- **RTO (Recovery Time Objective)** — Maximum acceptable downtime
- **Backup Testing** — Regular restore drills, verify backups actually work
- **Point-in-Time Recovery (PITR)** — Database WAL replay, continuous archiving

### Failover Strategies
- **Active-Passive** — Standby takes over on primary failure, cold/warm/hot standby
- **Active-Active** — Multiple active regions, traffic split, conflict resolution needed
- **DNS Failover** — Route53 health checks, failover routing policies
- **Database Failover** — Automatic promotion of replicas, split-brain prevention
- **Multi-Region** — Cross-region replication, regional isolation, global load balancing

### Disaster Recovery Tiers
- **Backup & Restore** — Cheapest, slowest recovery (hours)
- **Pilot Light** — Minimal always-on infrastructure, scale up on failure
- **Warm Standby** — Scaled-down copy of production, faster failover (minutes)
- **Multi-Site Active-Active** — Full redundancy, near-zero downtime, highest cost

### Business Continuity
- **DR Runbooks** — Step-by-step recovery procedures per service
- **DR Drills** — Regular simulated failovers, tabletop exercises
- **Dependency Mapping** — Know your critical path and upstream/downstream dependencies
- **Blast Radius Reduction** — Cell-based architecture, shuffle sharding, failure domains

---

## [[Traffic Management]]

### Traffic Shifting
- **Weighted Routing** — Gradually shift traffic between deployments (see [[CI-CD]])
- **Traffic Mirroring / Shadowing** — Duplicate production traffic to test environment without affecting users
- **Dark Traffic** — Send real traffic to new service version, discard responses, compare
- **Geographic Routing** — Route users to nearest region, latency-based routing

### Load Shedding
- **Priority-Based Shedding** — Drop low-priority requests under load to protect critical paths
- **Admission Control** — Reject requests early when system is at capacity
- **Throttling** — Per-client rate limits, adaptive throttling based on system health
- **Backpressure Propagation** — Signal upstream to slow down rather than buffering until OOM

### Configuration Management in Production
- **Feature Flags** — Runtime configuration changes without deploys (see [[CI-CD]])
- **Dynamic Configuration** — Config servers (Consul, etcd), runtime tuning without restarts
- **Configuration Drift** — Detect and remediate drift between intended and actual state
- **Secrets Rotation** — Automated rotation of credentials, certificates, API keys

---

## [[Performance Engineering]]

### Profiling
- **CPU Profiling** — Flame graphs, sampling profilers (perf, pprof, py-spy, async-profiler)
- **Memory Profiling** — Heap analysis, memory leaks, allocation tracking
- **I/O Profiling** — Disk I/O, network I/O, database query analysis
- **Application Performance Monitoring (APM)** — Datadog, New Relic, Dynatrace

### Benchmarking
- **Micro-Benchmarks** — Test individual functions (JMH for Java, BenchmarkDotNet, criterion for Rust)
- **Macro-Benchmarks** — System-level performance testing
- **Statistical Rigor** — Warm-up, iterations, percentiles, variance
- **Comparison Testing** — A/B performance comparisons, regression detection

### Load Testing
- **Tools** — k6, Locust, Gatling, JMeter, Artillery, wrk
- **Test Types** — Load test, stress test, soak test, spike test, breakpoint test
- **Traffic Patterns** — Ramp-up, steady state, spike, diurnal patterns
- **Metrics to Watch** — Latency percentiles, throughput, error rate, resource utilization

### Capacity Planning
- **Forecasting** — Historical trends, growth projections
- **Headroom** — Buffer for traffic spikes, typically 2-3x average
- **Auto-Scaling** — Horizontal (add instances), vertical (bigger instances)
- **Cost Optimization** — Right-sizing, reserved instances, spot instances, serverless economics

### Chaos Engineering
- **Principles** — Define steady state, hypothesize, introduce failures, observe
- **Chaos Monkey** — Randomly terminate instances (Netflix)
- **Litmus Chaos / Chaos Mesh** — Kubernetes-native chaos tools
- **Game Days** — Planned chaos experiments with the team
- **Failure Injection** — Network partitions, latency injection, disk failure, DNS failure

### Performance Optimization Patterns
- **Caching** — See [[Caching]] in Data Management
- **Connection Pooling** — Reuse database/HTTP connections
- **Async Processing** — Move work off the hot path, use queues
- **Batch Processing** — Amortize overhead across multiple items
- **Denormalization** — Trade storage for read performance
- **Read Replicas** — Scale reads horizontally
- **Compression** — gzip, Brotli, zstd for network transfer
- **Lazy Loading** — Load data only when needed

---

#reliability #sre #operations #observability #performance #disaster-recovery #traffic-management
