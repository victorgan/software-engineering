# Exponential Backoff

> <- Back to [[Retries with Backoff]]

A retry strategy where the delay between retries increases exponentially (e.g., 1s, 2s, 4s, 8s). This prevents overwhelming a recovering service with retry storms. Combined with jitter (random variation), it spreads retry load over time.

#sre #retries #backoff
