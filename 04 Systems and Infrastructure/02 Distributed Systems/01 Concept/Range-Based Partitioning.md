# Range-Based Partitioning

> <- Back to [[Partitioning and Sharding]]

Partitioning data by key ranges (e.g., A-M on partition 1, N-Z on partition 2). Enables efficient range queries since adjacent keys are on the same partition. Risk of hotspots if certain key ranges are accessed much more frequently. Used by HBase, BigTable, and some SQL databases.

## Key Properties

- [[Range Queries]]
- [[Hotspot Risk]]
- [[Sequential Key Problems]]

## Related

- [[Hash-Based Partitioning]] (eliminates hotspots but loses range query efficiency)
- [[Rebalancing]] (range splits when partitions grow too large)

---

#distributed-systems #sharding
