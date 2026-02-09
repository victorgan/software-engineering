# Sequential Consistency

> <- Back to [[Memory Ordering]]

The strongest memory ordering: all threads observe all operations in a single total order consistent with each thread's program order. Simplest to reason about but most restrictive for hardware optimization. The default in Java and C++ `memory_order_seq_cst`.

#concurrency #lock-free #memory-ordering #sequential
