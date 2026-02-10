# Tail-Based Sampling

> <- Back to [[Trace Sampling]]

Sampling decision made after request completion, allowing selection based on outcome (errors, high latency, specific attributes). More complex to implement as it requires buffering complete traces, but captures all interesting traces regardless of overall sample rate.

#observability #tracing #sampling
