# Mutexes - Locks

> <- Back to [[Synchronization Primitives]]

Mutual exclusion primitives that ensure only one thread can hold the lock at a time. A thread must acquire the mutex before entering a critical section and release it when done. Failure to release causes deadlock; holding too long causes contention.

## Key Properties

- [[Mutual Exclusion]]
- [[One Thread Holds Lock at a Time]]

---

#concurrency #synchronization #mutex
