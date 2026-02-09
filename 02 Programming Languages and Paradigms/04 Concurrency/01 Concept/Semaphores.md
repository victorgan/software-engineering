# Semaphores

> <- Back to [[Synchronization Primitives]]

Counting-based synchronization primitives that maintain a count of available permits. Threads acquire (decrement) and release (increment) permits. A semaphore with count 1 is a binary semaphore (functionally similar to a mutex). Used to limit concurrent access to a resource pool.

## Key Properties

- [[Counting-based Access Control]]
- [[Limit Concurrent Access]]

---

#concurrency #synchronization #semaphore
