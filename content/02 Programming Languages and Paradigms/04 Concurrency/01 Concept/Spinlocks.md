# Spinlocks

> <- Back to [[Synchronization Primitives]]

Locks where the waiting thread continuously polls (spins) to check if the lock is available, rather than sleeping. Spinlocks are useful for very short critical sections where the overhead of putting a thread to sleep and waking it exceeds the expected wait time.

## Key Properties

- [[Busy-wait Locks]]
- [[Short Critical Sections]]

---

#concurrency #synchronization #spinlocks
