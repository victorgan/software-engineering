# Try-lock

> <- Back to [[Deadlock Prevention]]

A non-blocking lock acquisition attempt that returns immediately with success or failure rather than blocking. If the lock cannot be acquired, the thread can release held locks and retry, preventing the hold-and-wait condition.

#concurrency #deadlock #prevention #try-lock
