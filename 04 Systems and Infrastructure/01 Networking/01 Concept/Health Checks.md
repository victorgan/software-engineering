# Health Checks

> <- Back to [[Load Balancing]]

Mechanisms to verify backend servers are functioning correctly. Active health checks periodically probe backends with synthetic requests. Passive health checks monitor actual request responses for errors. Unhealthy servers are removed from the pool until they recover. Critical for high availability.

## Key Properties

- [[Active Probing]]
- [[Passive Monitoring]]
- [[Health Check Endpoints]]

## Related

- [[Load Balancing Algorithms]] (only healthy servers receive traffic)
- [[Circuit Breaker]] (similar failure detection at application level)

---

#networking #load-balancing #reliability
