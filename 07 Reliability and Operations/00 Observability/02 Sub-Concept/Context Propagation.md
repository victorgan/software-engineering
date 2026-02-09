# Context Propagation

> <- Back to [[Traces]]

The mechanism by which trace context (trace ID, span ID, baggage) is passed between services, typically via HTTP headers (W3C Trace Context, B3 headers). Without context propagation, traces break at service boundaries and lose their cross-service value.

#observability #traces #context-propagation
