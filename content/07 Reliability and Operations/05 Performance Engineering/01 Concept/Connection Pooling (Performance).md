# Connection Pooling (Performance)

> <- Back to [[Performance Optimization Patterns]]

Reusing database and HTTP connections rather than creating new ones for each request. Connection establishment is expensive (TCP handshake, TLS negotiation, authentication), so pooling amortizes this cost across many requests.

## Key Properties

- [[Pool Size Configuration]]
- [[Connection Lifecycle]]
- [[Pool Exhaustion Handling]]

---

#performance #optimization #connection-pooling
