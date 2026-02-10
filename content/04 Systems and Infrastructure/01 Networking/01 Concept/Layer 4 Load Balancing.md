# Layer 4 Load Balancing

> <- Back to [[Load Balancing]]

Load balancing at the transport layer (TCP/UDP) based on IP addresses and port numbers. Very fast since it does not inspect packet contents. Routes entire connections to a backend. Examples include HAProxy (L4 mode) and AWS Network Load Balancer (NLB). Cannot make content-based routing decisions.

## Key Properties

- [[TCP UDP Level Routing]]
- [[Connection-Based Forwarding]]
- [[High Performance L4]]

## Related

- [[Layer 7 Load Balancing]] (content-aware alternative)
- [[Transport Layer]] (the layer at which L4 LBs operate)

---

#networking #load-balancing
