# Green Threads - Fibers

> <- Back to [[Concurrency Models]]

User-space threads that are scheduled by the runtime rather than the OS kernel. Green threads are extremely lightweight (small stacks, fast creation), enabling millions of concurrent tasks. The runtime multiplexes green threads onto a smaller pool of OS threads.

## Key Properties

- [[User-space Threads]]
- [[Lightweight Scheduling]]

## Related

- Go goroutines, Erlang processes, Java virtual threads / Project Loom

---

#concurrency #models #green-threads #fibers
