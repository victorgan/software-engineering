# Hash-Based Sharding

> <- Back to [[Sharding Strategies]]

Hash the shard key, mod by shard count for even distribution. Downside: range queries must hit all shards (scatter-gather).

## Key Properties

- [[Hash and Mod Distribution]]
- [[Even Distribution]]
- [[Scatter-Gather for Range Queries]]

---

#sharding #hash-based
