# Cooperative Scheduling

> <- Back to [[Green Threads and Fibers]]

Green threads voluntarily yield control at specific points (I/O operations, explicit yield calls) rather than being preempted by the OS. This simplifies synchronization but means a misbehaving thread can starve others. Go's goroutine scheduler adds preemption points to mitigate this.

#operating-systems #green-threads #scheduling
