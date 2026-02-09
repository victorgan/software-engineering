# Shared Memory

> <- Back to [[Thread]]

Threads within the same process share the heap, global variables, and file descriptors. This makes inter-thread communication fast (no IPC needed) but introduces the need for synchronization primitives like mutexes and semaphores to avoid race conditions.

#operating-systems #threads #memory
