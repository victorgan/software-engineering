# Load Balancing Algorithms

> <- Back to [[Load Balancing]]

Strategies for distributing requests across backend servers. Round robin distributes evenly in order. Weighted round robin accounts for different server capacities. Least connections routes to the server with fewest active connections. IP hash routes the same client to the same server. Consistent hashing minimizes redistribution when servers change.

## Key Properties

- [[Round Robin LB]]
- [[Least Connections]]
- [[Consistent Hashing LB]]

## Related

- [[Session Affinity]] (routing the same user to the same server)
- [[Health Checks]] (only route to healthy servers)

---

#networking #load-balancing #algorithms
