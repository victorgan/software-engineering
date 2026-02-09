# ABA Problem

> <- Back to [[Lock-Free & Wait-Free Programming]]

A subtle bug in CAS-based algorithms where a value changes from A to B and back to A. The CAS operation sees the original value and succeeds, but the underlying state may have changed significantly. Solutions include tagged pointers (version counters) and hazard pointers.

## Key Properties

- [[Value Changes A to B to A]]
- [[CAS Doesn't Detect Intermediate Change]]

---

#concurrency #lock-free #aba
