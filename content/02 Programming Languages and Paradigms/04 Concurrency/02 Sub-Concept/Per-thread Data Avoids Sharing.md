# Per-thread Data Avoids Sharing

> <- Back to [[Thread-Local Storage]]

Each thread gets its own independent copy of a variable, eliminating the need for synchronization entirely. Thread-local data is useful for per-thread caches, connection pools, random number generators, and transaction contexts that are expensive to synchronize.

#concurrency #patterns #thread-local #no-sharing
