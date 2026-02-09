# Priority Inversion

> <- Back to [[Deadlocks & Livelocks]]

A scheduling anomaly where a high-priority thread is blocked because a low-priority thread holds a needed lock, and medium-priority threads prevent the low-priority thread from running. Priority inheritance (temporarily boosting the lock holder's priority) is the standard solution.

## Key Properties

- [[High-priority Blocked by Low-priority]]
- [[Priority Inheritance]]

---

#concurrency #priority-inversion
