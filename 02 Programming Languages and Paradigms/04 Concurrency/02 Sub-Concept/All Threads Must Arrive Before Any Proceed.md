# All Threads Must Arrive Before Any Proceed

> <- Back to [[Barriers]]

When a thread reaches a barrier, it blocks until all participating threads have also reached the barrier. Once all threads arrive, they are all released simultaneously. Used in iterative algorithms where each iteration depends on the previous one completing across all threads.

#concurrency #synchronization #barriers
