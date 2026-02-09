# Strong vs Eventual Consistency

> <- Back to [[Consistency vs Availability]]

Strong consistency guarantees that after a write completes, all subsequent reads return the updated value. Eventual consistency guarantees that given enough time without new updates, all replicas will converge. Most real-world systems use eventual consistency for availability and performance.

#property #tradeoffs #consistency
