# Read-Write Locks

> <- Back to [[Synchronization Primitives]]

Locks that distinguish between read access and write access. Multiple threads can hold read locks concurrently (since reads don't conflict), but write locks are exclusive. Ideal for read-heavy workloads where writes are infrequent.

## Key Properties

- [[Multiple Concurrent Readers]]
- [[Exclusive Writer]]

---

#concurrency #synchronization #rwlock
