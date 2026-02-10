# Readers-Writer Pattern

> <- Back to [[Concurrency Hazards & Patterns]]

A pattern allowing multiple concurrent readers but only a single writer at a time. Readers can proceed in parallel since they don't modify data, while writers require exclusive access. Implemented using read-write locks.

## Key Properties

- [[Multiple Readers Single Writer]]

---

#concurrency #patterns #readers-writer
