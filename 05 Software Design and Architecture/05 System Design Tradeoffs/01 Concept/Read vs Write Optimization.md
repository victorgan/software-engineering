# Read vs Write Optimization

> <- Back to [[Fundamental Tradeoffs]]

Denormalization and caching speed reads at the cost of write complexity. Normalized data is easier to write but requires joins for reads. The read-to-write ratio of your workload should drive the optimization direction.

## Key Properties

- [[Denormalization Tradeoff]]
- [[Caching Strategy]]
- [[Read-Write Ratio]]

## Related

- [[CQRS]] (separate optimization for each)

---

#tradeoffs #read-write #optimization
