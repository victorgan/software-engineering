# Thread-Local Storage

> <- Back to [[Concurrency Hazards & Patterns]]

Per-thread data that is not shared between threads, avoiding synchronization entirely. Each thread gets its own copy of thread-local variables. Useful for thread-specific contexts, caches, random number generators, and database connections.

## Key Properties

- [[Per-thread Data Avoids Sharing]]

---

#concurrency #patterns #thread-local
