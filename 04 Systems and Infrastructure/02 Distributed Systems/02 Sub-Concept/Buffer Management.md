# Buffer Management

> <- Back to [[Backpressure]]

Queues act as buffers between producers and consumers, absorbing temporary rate mismatches. Buffer strategies: bounded buffers (reject when full, providing backpressure), unbounded buffers (risk memory exhaustion), and overflow to persistent storage (durable but slower). Monitoring queue depth is critical for detecting backpressure issues.

#distributed-systems #messaging
