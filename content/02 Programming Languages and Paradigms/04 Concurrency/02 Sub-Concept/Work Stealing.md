# Work Stealing

> <- Back to [[Fork-Join]]

A load-balancing strategy where idle threads steal tasks from the queues of busy threads. Each thread has a deque of tasks; it processes from its own deque, and when empty, steals from the tail of another thread's deque. Used in Java's ForkJoinPool and Rust's rayon.

#concurrency #data-parallelism #fork-join #work-stealing
