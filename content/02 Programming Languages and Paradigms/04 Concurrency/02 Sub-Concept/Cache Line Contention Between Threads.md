# Cache Line Contention Between Threads

> <- Back to [[False Sharing]]

When threads on different cores modify variables that share the same cache line, the cache coherency protocol bounces the line between cores on every write. This can degrade performance dramatically despite no logical data sharing. Padding variables to separate cache lines eliminates false sharing.

#concurrency #hazards #false-sharing #cache-line
