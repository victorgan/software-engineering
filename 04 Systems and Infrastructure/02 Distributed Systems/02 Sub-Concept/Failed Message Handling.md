# Failed Message Handling

> <- Back to [[Dead Letter Queues]]

When a message fails processing after the maximum retry count, it is moved to the DLQ instead of being discarded or blocking the queue. This preserves the failed message for debugging and reprocessing while allowing the main queue to continue processing new messages.

#distributed-systems #messaging
