# Busy-wait Locks

> <- Back to [[Spinlocks]]

Instead of sleeping when the lock is unavailable, the thread continuously loops (spins) checking the lock's state. This avoids the overhead of context switching into the kernel but wastes CPU cycles. Efficient only when the expected wait time is shorter than the cost of sleeping.

#concurrency #synchronization #spinlocks #busy-wait
