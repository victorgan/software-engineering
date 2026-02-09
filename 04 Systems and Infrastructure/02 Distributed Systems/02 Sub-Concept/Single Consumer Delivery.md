# Single Consumer Delivery

> <- Back to [[Point-to-Point Messaging]]

Each message is delivered to and processed by exactly one consumer, even if multiple consumers are listening on the queue. The queue acts as a load balancer, distributing messages across available consumers. After acknowledgment, the message is removed from the queue.

#distributed-systems #messaging
