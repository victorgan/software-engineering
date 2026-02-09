# Heaps

> ← Back to [[Tree Structures]]

Complete binary tree satisfying the heap property — parent is always greater (max-heap) or smaller (min-heap) than children. Primary implementation of priority queues.

## Key Properties

- [[Min-Heap]]
- [[Max-Heap]]
- [[Binary Heap]]
- [[Fibonacci Heap]]

## Complexity

| Operation       | Time Complexity                          |
| --------------- | ---------------------------------------- |
| Insert          | O(log n)                                 |
| Extract-min/max | O(log n)                                 |
| Peek            | O(1)                                     |
| Build heap      | O(n)                                     |
| Decrease-key    | O(log n) [O(1) amortized for Fibonacci]  |

## Related

- [[Priority Queues]] (abstract interface)
- [[Queues]]
- [[Heap Sort]]

---

#data-structures #trees #heaps
