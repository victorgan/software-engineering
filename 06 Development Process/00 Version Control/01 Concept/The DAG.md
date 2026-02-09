# The DAG

> <- Back to [[Git Internals]]

The Directed Acyclic Graph of commit history. Each commit points to its parent(s), forming a graph that can never have cycles. Merge commits have multiple parents. Understanding the DAG is key to understanding rebasing, merging, and history manipulation.

## Key Properties

- [[Parent Pointers]]
- [[Merge Points]]
- [[History Graph]]

## Related

- [[Refs]] (entry points into the DAG)
- [[Rebase]] (rewrites the DAG)

---

#git #internals #dag
