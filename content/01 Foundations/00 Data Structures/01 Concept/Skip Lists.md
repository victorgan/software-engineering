# Skip Lists

> ← Back to [[Advanced Structures]]

Probabilistic data structure that layers multiple sorted linked lists with express lanes for faster traversal. A simpler alternative to balanced BSTs with similar average-case guarantees.

## Key Properties

- [[Probabilistic Balancing]]

## Complexity

- Search O(log n), Insert O(log n), Delete O(log n) — all expected.

## Used In

- Redis sorted sets
- LevelDB/RocksDB memtables

## Related

- [[Linked Lists]] (built on)
- [[Self-Balancing Trees]] (alternative)
- [[Binary Search Trees]]

---

#data-structures #advanced #skip-lists
