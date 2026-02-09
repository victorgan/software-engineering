# Data Races

> <- Back to [[Concurrency Hazards & Patterns]]

Unsynchronized access to shared mutable data where at least one access is a write. Data races cause undefined behavior in C/C++ and Rust (prevented at compile time). Distinguished from race conditions: data races are a specific low-level hazard, while race conditions are higher-level logic bugs.

## Key Properties

- [[Unsynchronized Access to Shared Mutable Data]]

---

#concurrency #hazards #data-races
