# User-Space Scheduling

> <- Back to [[Green Threads and Fibers]]

The runtime (not the OS kernel) manages scheduling of green threads. This avoids system call overhead for thread creation and context switching, enabling millions of concurrent tasks. The runtime multiplexes green threads onto a smaller pool of OS threads.

#operating-systems #green-threads #scheduling
