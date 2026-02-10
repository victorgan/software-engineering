# Rate Limiting

> <- Back to [[API Gateway]]

Controlling the number of requests a client can make within a time window. Common algorithms: fixed window (simple but bursty at boundaries), sliding window (smooth), token bucket (allows bursts up to a limit), leaky bucket (constant rate). Returns 429 Too Many Requests when exceeded.

#networking #api-gateway
