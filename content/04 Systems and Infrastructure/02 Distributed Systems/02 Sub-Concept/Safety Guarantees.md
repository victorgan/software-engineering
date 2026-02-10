# Safety Guarantees

> <- Back to [[Raft]]

Raft guarantees: (1) election safety — at most one leader per term, (2) leader append-only — leaders never overwrite log entries, (3) log matching — if two logs contain an entry with the same index and term, all preceding entries are identical, (4) state machine safety — committed entries are applied identically.

#distributed-systems #consensus
