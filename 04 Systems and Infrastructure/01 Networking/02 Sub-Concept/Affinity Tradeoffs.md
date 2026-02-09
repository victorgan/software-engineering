# Affinity Tradeoffs

> <- Back to [[Session Affinity]]

Sticky sessions simplify stateful applications but create uneven load distribution (popular users create hotspots), complicate scaling (sessions are lost on server failure), and reduce the benefit of having multiple backends. The better architectural approach is to externalize session state (Redis, database).

#networking #load-balancing
