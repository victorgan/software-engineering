# Lifetimes

> <- Back to [[Ownership & Borrowing (Rust Model)]]

Compile-time annotations that track how long references are valid. Lifetimes ensure that references never outlive the data they point to, preventing dangling references. The borrow checker uses lifetime analysis to verify reference safety without runtime checks.

## Key Properties

- [[Compile-time Tracking of Reference Validity]]

---

#memory-models #rust #lifetimes
