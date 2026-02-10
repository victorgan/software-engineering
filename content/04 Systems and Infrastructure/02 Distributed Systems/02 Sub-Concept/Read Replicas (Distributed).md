# Read Replicas (Distributed)

> <- Back to [[Single-Leader Replication]]

Follower nodes that receive replicated writes from the leader and serve read queries. Scale read throughput by adding more replicas. May serve slightly stale data due to replication lag (eventual consistency for reads). Common in database deployments (PostgreSQL streaming replicas, MySQL read replicas).

#distributed-systems #replication
