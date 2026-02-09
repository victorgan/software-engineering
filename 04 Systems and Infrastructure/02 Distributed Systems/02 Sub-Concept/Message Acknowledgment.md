# Message Acknowledgment

> <- Back to [[Point-to-Point Messaging]]

Consumers explicitly acknowledge (ACK) successful processing. Unacknowledged messages (due to consumer crash or timeout) are redelivered. This ensures no messages are lost, providing at-least-once delivery. Negative acknowledgment (NACK) can trigger immediate redelivery or routing to a dead letter queue.

#distributed-systems #messaging
