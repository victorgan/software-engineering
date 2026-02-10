# Sequential Consistency (Distributed)

> <- Back to [[Consistency Models]]

All processes see the same order of operations, but that order does not need to match real-time. Operations from each process maintain their program order, but interleaving between processes can differ from wall-clock order. Weaker than linearizability but still provides a global total order.

## Key Properties

- [[Global Total Order]]
- [[Program Order Preservation]]
- [[Non-Real-Time Ordering]]

## Related

- [[Strong Consistency]] (stronger — respects real-time order)
- [[Causal Consistency]] (weaker — only orders causally related operations)

---

#distributed-systems #consistency
