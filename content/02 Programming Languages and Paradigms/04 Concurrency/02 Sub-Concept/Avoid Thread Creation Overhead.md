# Avoid Thread Creation Overhead

> <- Back to [[Thread Pools]]

Creating an OS thread involves kernel calls, stack allocation, and scheduler registration. By reusing pre-created threads, thread pools amortize this cost across many tasks. This is essential for handling high-throughput workloads like web servers processing many short-lived requests.

#concurrency #patterns #thread-pools #overhead
