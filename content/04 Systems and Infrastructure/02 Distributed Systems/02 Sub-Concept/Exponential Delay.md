# Exponential Delay

> <- Back to [[Retry with Exponential Backoff]]

Each retry waits exponentially longer: delay = base * 2^attempt (e.g., 1s, 2s, 4s, 8s, 16s). This gives the failing service increasingly more time to recover and reduces load on it. Without backoff, aggressive retries can overwhelm a struggling service (retry storm).

#distributed-systems #patterns #resilience
