# Timeout-based Acquisition

> <- Back to [[Deadlock Prevention]]

Attempting to acquire a lock with a timeout. If the lock is not obtained within the specified time, the thread gives up, releases any held locks, and retries later. This breaks the hold-and-wait condition and prevents indefinite blocking.

#concurrency #deadlock #prevention #timeout
