# Consumer Rate Limiting

> <- Back to [[Backpressure]]

Consumers control their own processing rate by pulling messages at their own pace (pull-based) rather than having messages pushed to them (push-based). Kafka uses a pull model where consumers control their position and rate. This naturally prevents overwhelming slow consumers.

#distributed-systems #messaging
