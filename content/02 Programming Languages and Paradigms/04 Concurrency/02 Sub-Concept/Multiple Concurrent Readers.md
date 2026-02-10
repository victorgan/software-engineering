# Multiple Concurrent Readers

> <- Back to [[Read-Write Locks]]

Read-write locks allow any number of threads to hold read locks simultaneously, since concurrent reads don't conflict. This provides much better throughput than a mutex for read-heavy workloads where writes are infrequent.

#concurrency #synchronization #rwlock #readers
