# Unable to Acquire Resources Due to Unfair Scheduling

> <- Back to [[Thread Starvation]]

Some threads may never get to run if the scheduler consistently favors other threads. Unfair lock implementations, priority-based scheduling without aging, and thread pools with unbounded queues can all lead to starvation of certain threads.

#concurrency #hazards #starvation #scheduling
