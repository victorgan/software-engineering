# Every Thread Makes Progress in Bounded Steps

> <- Back to [[Wait-Free Algorithms]]

Wait-free is the strongest non-blocking guarantee: every thread completes its operation in a finite number of steps, regardless of contention or scheduling. This is stronger than lock-free, which only guarantees that some thread makes progress. Wait-free algorithms are harder to implement but provide deterministic latency.

#concurrency #wait-free #bounded-progress
