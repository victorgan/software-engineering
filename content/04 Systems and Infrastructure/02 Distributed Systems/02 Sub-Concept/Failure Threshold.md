# Failure Threshold

> <- Back to [[Circuit Breaker]]

The circuit opens when the error rate exceeds a configured threshold (e.g., 50% errors in a 10-second window, or 5 consecutive failures). The threshold should be tuned based on the service's normal error rate and the acceptable impact of false positives (opening when the service is actually healthy).

#distributed-systems #patterns #resilience
