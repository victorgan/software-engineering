# High-priority Blocked by Low-priority

> <- Back to [[Priority Inversion]]

A high-priority thread needing a lock held by a low-priority thread must wait. If medium-priority threads preempt the low-priority thread, the high-priority thread is effectively blocked by medium-priority threads indefinitely — an inversion of the priority ordering.

#concurrency #priority-inversion #blocking
