# Paxos

> <- Back to [[Consensus Algorithms]]

The classic consensus algorithm by Leslie Lamport. Proposers, acceptors, and learners work together to agree on a value. Correct and proven but notoriously difficult to understand and implement. Many real-world systems use Paxos variants (Multi-Paxos, Cheap Paxos). Google's Chubby lock service uses Paxos internally.

## Key Properties

- [[Proposer Acceptor Learner Roles]]
- [[Majority Agreement]]
- [[Multi-Paxos]]

## Related

- [[Raft]] (designed as an understandable alternative to Paxos)
- [[Zab]] (ZooKeeper's alternative approach)

---

#distributed-systems #consensus
