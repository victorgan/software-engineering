# Latency Reality

> <- Back to [[Fallacies of Distributed Computing]]

Network calls have measurable latency: ~0.5ms within a datacenter, ~50-100ms cross-region, ~100-300ms cross-continent. Tail latencies (p99, p999) can be orders of magnitude higher. A system making 100 sequential network calls amplifies latency dramatically. Design for latency with caching, batching, and parallelism.

#distributed-systems #fundamentals #performance
