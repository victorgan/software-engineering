# Layer 7 Load Balancing

> <- Back to [[Load Balancing]]

Load balancing at the application layer (HTTP) that can inspect request contents. Enables content-based routing (URL path, headers, cookies), SSL termination, and request modification. Examples include Nginx, AWS ALB, and Envoy. More flexible but higher latency than L4.

## Key Properties

- [[Content-Based Routing]]
- [[SSL Termination]]
- [[Header Inspection]]

## Related

- [[Layer 4 Load Balancing]] (simpler, faster alternative)
- [[Application Layer]] (the layer at which L7 LBs operate)

---

#networking #load-balancing
