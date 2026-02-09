# Lazy Initialization Pattern

> <- Back to [[Double-Checked Locking]]

Defer the creation of an expensive object until it is first needed. Double-checked locking checks for initialization without a lock first (fast path), then acquires a lock and checks again before initializing (slow path). Requires careful memory ordering to be correct.

#concurrency #patterns #lazy-initialization
