# TTL

> <- Back to [[DNS]]

Time To Live — the duration (in seconds) that a DNS record can be cached before it must be re-queried. Short TTLs (60s) enable fast failover but increase DNS query load. Long TTLs (86400s) reduce load but slow down DNS changes. Propagation delays occur because caches expire at different times.

## Key Properties

- [[Caching Duration]]
- [[Propagation Delays]]
- [[TTL Strategies]]

## Related

- [[Resolution Process]] (TTL controls caching at each resolver)
- [[Record Types]] (each record has its own TTL)

---

#networking #dns
