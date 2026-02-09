# Relaxed Ordering

> <- Back to [[Memory Ordering]]

The weakest memory ordering: guarantees only atomicity of the operation itself, not ordering relative to other operations. Allows maximum hardware optimization (out-of-order execution, store buffering). Suitable for independent counters where relative ordering doesn't matter.

#concurrency #lock-free #memory-ordering #relaxed
