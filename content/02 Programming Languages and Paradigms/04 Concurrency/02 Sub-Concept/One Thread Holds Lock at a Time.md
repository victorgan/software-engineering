# One Thread Holds Lock at a Time

> <- Back to [[Mutexes - Locks]]

At most one thread can own a mutex at any moment. Other threads attempting to acquire the same mutex will block (sleep) until the owning thread releases it. This serialization is the core mechanism for protecting shared mutable state.

#concurrency #synchronization #mutex #exclusive
