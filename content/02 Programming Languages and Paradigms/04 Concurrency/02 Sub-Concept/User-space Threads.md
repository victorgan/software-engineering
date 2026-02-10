# User-space Threads

> <- Back to [[Green Threads - Fibers]]

Threads managed by the language runtime rather than the OS kernel. Creation takes microseconds (vs milliseconds for OS threads), stack sizes are small and growable (kilobytes vs megabytes), and context switching avoids kernel transitions. The runtime multiplexes thousands or millions of green threads onto a few OS threads.

#concurrency #models #green-threads #user-space
