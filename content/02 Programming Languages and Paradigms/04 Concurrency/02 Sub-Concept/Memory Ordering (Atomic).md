# Memory Ordering (Atomic)

> <- Back to [[Atomic Operations]]

Atomic operations accept a memory ordering parameter that specifies visibility guarantees. This controls which other memory operations can be reordered around the atomic operation by the compiler and hardware, trading correctness guarantees for performance.

#concurrency #lock-free #atomic #ordering
