# Work Queue Pattern

> <- Back to [[Point-to-Point Messaging]]

Multiple worker processes consume from the same queue, processing tasks in parallel. Work is automatically distributed across workers. Adding more workers scales processing capacity. If a worker crashes, unacknowledged messages are redelivered to another worker.

#distributed-systems #messaging
