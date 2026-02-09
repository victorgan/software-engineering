# OR-Set

> <- Back to [[CRDTs]]

Observed-Remove Set — a CRDT set that handles concurrent add and remove operations. Each element is tagged with a unique identifier. Removes only affect observed instances (with specific tags), so a concurrent add of the same element is not affected by the remove. Provides intuitive set semantics without conflicts.

#distributed-systems #crdts
