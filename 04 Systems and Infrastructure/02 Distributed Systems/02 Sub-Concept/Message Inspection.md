# Message Inspection

> <- Back to [[Dead Letter Queues]]

DLQ messages can be inspected to diagnose failures: examining the message body, headers, error information, and retry count. After fixing the underlying issue (code bug, dependency failure, data issue), messages can be replayed from the DLQ back to the main queue for reprocessing.

#distributed-systems #messaging
