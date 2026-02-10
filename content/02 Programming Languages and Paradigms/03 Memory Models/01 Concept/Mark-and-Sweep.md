# Mark-and-Sweep

> <- Back to [[Garbage Collection (GC)]]

A GC algorithm with two phases: mark (trace all reachable objects starting from roots) and sweep (free all unmarked/unreachable objects). Simple and handles cycles naturally, but requires stopping the world during collection and can cause fragmentation.

## Key Properties

- [[Trace Reachable Objects]]
- [[Free Unreachable]]

---

#memory-models #gc #mark-and-sweep
