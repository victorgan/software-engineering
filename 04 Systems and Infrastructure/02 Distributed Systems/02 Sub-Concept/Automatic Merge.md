# Automatic Merge

> <- Back to [[CRDTs]]

CRDTs are mathematically guaranteed to converge to the same state regardless of the order in which updates are received. The merge function is commutative, associative, and idempotent. No coordination, conflict resolution logic, or human intervention is needed. The data structure's design prevents conflicts by construction.

#distributed-systems #crdts
