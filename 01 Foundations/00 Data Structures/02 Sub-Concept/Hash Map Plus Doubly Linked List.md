# Hash Map Plus Doubly Linked List

> ← Back to [[LRU Cache]]

The hash map provides O(1) key lookup. The doubly linked list maintains access order, with the most recently used at the head. On access, move the node to the head. On eviction, remove the tail. Both operations are O(1).

#property #caching
