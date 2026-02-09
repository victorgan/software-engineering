# Jitter

> <- Back to [[Retry with Exponential Backoff]]

Adding randomness to retry delays to prevent thundering herd: many clients retrying at the exact same time. Full jitter: delay = random(0, base * 2^attempt). Decorrelated jitter: delay = random(base, previous_delay * 3). AWS recommends jitter for all retry strategies.

#distributed-systems #patterns #resilience
