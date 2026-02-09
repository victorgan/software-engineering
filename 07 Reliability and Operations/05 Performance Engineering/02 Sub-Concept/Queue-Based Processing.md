# Queue-Based Processing

> <- Back to [[Async Processing]]

Using message queues (SQS, RabbitMQ, Kafka) to decouple request handling from background processing. Producers enqueue work items; consumers process them asynchronously. This pattern absorbs traffic spikes, enables retry logic, and decouples services.

#performance #optimization #queues
