# Mutex Plus Condition Variables

> <- Back to [[Monitors]]

A monitor combines a mutex (for mutual exclusion) with condition variables (for waiting and signaling). Java's `synchronized` blocks implement monitors, where `wait()` releases the lock and blocks, and `notify()`/`notifyAll()` wake waiting threads.

#concurrency #synchronization #monitors
