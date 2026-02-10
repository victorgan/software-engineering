# Byzantine Fault Tolerance

> <- Back to [[Consensus Algorithms]]

Handling nodes that can behave arbitrarily (malicious or buggy), not just crash. The Byzantine Generals Problem: reaching agreement when some generals may be traitors. PBFT (Practical BFT) tolerates up to f failures with 3f+1 nodes. Used in blockchain consensus and high-security systems. Much more expensive than crash-fault-tolerant consensus.

## Key Properties

- [[Byzantine Generals Problem]]
- [[PBFT Algorithm]]
- [[Blockchain Consensus]]

## Related

- [[Raft]] (only handles crash failures, not Byzantine)
- [[Paxos]] (also assumes non-Byzantine failures)

---

#distributed-systems #consensus #security
