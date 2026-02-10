# Head-Based Sampling

> <- Back to [[Trace Sampling]]

Sampling decision made at the beginning of a request before any processing occurs. Simple to implement (e.g., sample 10% of requests) but may miss interesting traces like errors or slow requests that happen to fall in the unsampled portion.

#observability #tracing #sampling
