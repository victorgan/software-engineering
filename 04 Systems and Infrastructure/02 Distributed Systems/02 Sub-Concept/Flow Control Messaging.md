# Flow Control Messaging

> <- Back to [[Backpressure]]

Mechanisms for producers to learn they should slow down: blocking when the queue is full, returning errors (HTTP 429, gRPC RESOURCE_EXHAUSTED), or using reactive streams protocols that let consumers request only what they can handle (Reactive Streams, gRPC flow control).

#distributed-systems #messaging
