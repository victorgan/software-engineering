# Causal Consistency

> <- Back to [[Consistency Models]]

Operations that are causally related (one depends on or is aware of another) are seen in the same order by all nodes. Concurrent operations (no causal relationship) may be seen in different orders by different nodes. Captures the intuitive "if you saw X before writing Y, everyone who sees Y also sees X."

## Key Properties

- [[Causal Ordering]]
- [[Concurrent Operations]]
- [[Causal Dependencies]]

## Related

- [[Sequential Consistency]] (stronger — orders all operations)
- [[Vector Clocks]] (mechanism for tracking causal relationships)

---

#distributed-systems #consistency
