# Lightweight Scheduling

> <- Back to [[Green Threads - Fibers]]

The runtime's scheduler maps green threads to OS threads using M:N threading (M green threads on N OS threads). Work-stealing schedulers (like Go's) balance load across OS threads. This provides concurrency without the overhead of one OS thread per task.

#concurrency #models #green-threads #scheduling
