# Exclusive Writer

> <- Back to [[Read-Write Locks]]

When a thread acquires a write lock, no other thread can hold either a read or write lock. The writer has exclusive access to the data, ensuring that reads see a consistent state and writes don't conflict.

#concurrency #synchronization #rwlock #writer
