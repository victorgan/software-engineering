# LRU Cache

> ← Back to [[Advanced Structures]]

Cache eviction strategy that removes the least recently used item when the cache is full. Implemented as a hash map (for O(1) lookup) combined with a doubly linked list (for O(1) eviction/reordering).

## Key Properties

- [[Hash Map Plus Doubly Linked List]]

## Complexity

- Get O(1), Put O(1), Evict O(1)

## Related

- [[Hash Tables]]
- [[Linked Lists]]
- [[Caching]] (application-level caching)

---

#data-structures #advanced #caching
