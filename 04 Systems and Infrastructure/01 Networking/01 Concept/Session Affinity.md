# Session Affinity

> <- Back to [[Load Balancing]]

Also called sticky sessions — routing requests from the same client to the same backend server. Necessary when server-side session state is not shared. Implemented via cookies, IP hashing, or consistent hashing. Trade-off: simplifies state management but reduces load distribution and complicates failover.

## Key Properties

- [[Sticky Session Cookies]]
- [[IP-Based Affinity]]
- [[Affinity Tradeoffs]]

## Related

- [[Load Balancing Algorithms]] (affinity constrains algorithm choice)
- [[Cookies and Sessions]] (session data drives affinity need)

---

#networking #load-balancing
