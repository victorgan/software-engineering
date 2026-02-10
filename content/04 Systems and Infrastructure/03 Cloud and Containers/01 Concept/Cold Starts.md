# Cold Starts

> <- Back to [[Serverless]]

The latency experienced when a function is invoked after being idle — the runtime must be initialized, code loaded, and dependencies started. Can add 100ms to several seconds depending on runtime and package size. Mitigated by provisioned concurrency (pre-warmed instances), smaller packages, and lighter runtimes.

## Key Properties

- [[Initialization Latency]]
- [[Provisioned Concurrency]]
- [[Runtime Impact]]

## Related

- [[Functions as a Service]] (cold starts are inherent to FaaS)
- [[Serverless Limitations]] (cold starts are a key limitation)

---

#cloud #serverless #performance
