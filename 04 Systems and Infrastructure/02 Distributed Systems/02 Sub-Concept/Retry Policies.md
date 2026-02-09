# Retry Policies

> <- Back to [[Dead Letter Queues]]

Configuration for how many times and how quickly to retry a failed message before sending it to the DLQ. Typically uses exponential backoff with jitter. Common policy: retry 3-5 times with increasing delays (1s, 5s, 30s), then move to DLQ. Must consider idempotency for retried messages.

#distributed-systems #messaging
