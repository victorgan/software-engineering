# High Cardinality

> <- Back to [[Choosing a Shard Key]]

The shard key should have many distinct values to distribute data evenly. user_id is good (millions of values), country is bad (few values leading to large skewed shards).

---

#sharding #shard-key #cardinality
