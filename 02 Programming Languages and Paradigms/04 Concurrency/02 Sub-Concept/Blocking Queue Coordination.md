# Blocking Queue Coordination

> <- Back to [[Producer-Consumer]]

A thread-safe queue that blocks on dequeue when empty and on enqueue when full. Java's BlockingQueue, Go's buffered channels, and Python's queue.Queue implement this pattern, providing the synchronization between producers and consumers automatically.

#concurrency #patterns #producer-consumer #blocking-queue
