# Counting-based Access Control

> <- Back to [[Semaphores]]

A semaphore maintains an integer count. `acquire()` decrements the count (blocking if zero), and `release()` increments it. The count represents the number of available permits, limiting how many threads can access a resource concurrently.

#concurrency #synchronization #semaphore #counting
