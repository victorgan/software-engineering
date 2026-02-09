# Strong Consistency

> <- Back to [[Consistency Models]]

Also called linearizability — reads always return the most recent write. The system behaves as if there is a single copy of the data. Requires coordination between replicas (quorum writes/reads or consensus), increasing latency. Used when correctness is critical (financial transactions, locks).

## Key Properties

- [[Linearizability]]
- [[Quorum Operations]]
- [[Coordination Cost]]

## Related

- [[Sequential Consistency]] (slightly weaker — same order, not necessarily real-time)
- [[Eventual Consistency]] (opposite end of the spectrum)

---

#distributed-systems #consistency
