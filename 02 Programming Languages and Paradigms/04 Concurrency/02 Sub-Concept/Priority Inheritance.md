# Priority Inheritance

> <- Back to [[Priority Inversion]]

The standard solution to priority inversion: when a high-priority thread blocks on a lock held by a low-priority thread, the low-priority thread temporarily inherits the high priority, preventing medium-priority threads from preempting it and allowing it to release the lock quickly.

#concurrency #priority-inversion #inheritance
