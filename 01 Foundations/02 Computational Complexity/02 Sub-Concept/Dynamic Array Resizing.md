# Dynamic Array Resizing

> <- Back to [[Amortized Analysis]]

When a dynamic array is full, it allocates a new array (typically double the size) and copies all elements. This single operation costs O(n), but since it happens infrequently (every n insertions), the amortized cost per insertion is O(1). The canonical example of amortized analysis.

#computational-complexity #time-complexity #amortized #dynamic-array
