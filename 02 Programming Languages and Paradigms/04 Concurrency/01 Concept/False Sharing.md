# False Sharing

> <- Back to [[Concurrency Hazards & Patterns]]

A performance problem where threads on different cores access different variables that happen to reside on the same cache line. Writes by one thread invalidate the cache line for all other threads, causing excessive cache coherency traffic despite no actual data sharing.

## Key Properties

- [[Cache Line Contention Between Threads]]

---

#concurrency #hazards #false-sharing
