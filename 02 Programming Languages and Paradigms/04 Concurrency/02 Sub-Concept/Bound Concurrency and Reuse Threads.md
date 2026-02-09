# Bound Concurrency and Reuse Threads

> <- Back to [[Thread Pools]]

A thread pool maintains a fixed (or bounded) number of worker threads. Tasks are submitted to a queue and processed by available threads. This bounds the maximum concurrent execution and reuses threads, preventing the overhead of creating and destroying threads for each task.

#concurrency #patterns #thread-pools #bounded
