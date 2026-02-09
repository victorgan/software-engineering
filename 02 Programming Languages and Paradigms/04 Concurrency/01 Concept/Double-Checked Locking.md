# Double-Checked Locking

> <- Back to [[Concurrency Hazards & Patterns]]

A pattern for lazy initialization in concurrent code: check if initialized (no lock), acquire lock, check again (with lock), then initialize. Historically broken in many languages due to memory model issues (instruction reordering). Requires volatile/atomic memory ordering to be correct.

## Key Properties

- [[Lazy Initialization Pattern]]
- [[Memory Model Pitfalls]]

---

#concurrency #patterns #double-checked-locking
