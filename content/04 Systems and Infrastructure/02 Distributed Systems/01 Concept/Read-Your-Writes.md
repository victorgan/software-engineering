# Read-Your-Writes

> <- Back to [[Consistency Models]]

A client always sees its own writes in subsequent reads, even if other clients may see stale data. A practical guarantee that prevents the confusing experience of submitting a form and not seeing your change. Can be implemented by routing reads to the same replica that accepted the write or tracking write timestamps.

## Key Properties

- [[Session Guarantees]]
- [[Write Visibility]]
- [[Implementation Strategies]]

## Related

- [[Eventual Consistency]] (read-your-writes is often layered on top)
- [[Session Affinity]] (routing mechanism to achieve this guarantee)

---

#distributed-systems #consistency
