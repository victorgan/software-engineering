# Ownership Rules

> <- Back to [[Ownership & Borrowing (Rust Model)]]

Rust's fundamental ownership rules: each value has exactly one owner, ownership can be transferred (moved) but not duplicated (unless the type implements Copy), and when the owner goes out of scope the value is dropped. These rules eliminate use-after-free and double-free at compile time.

## Key Properties

- [[Each Value Has One Owner]]
- [[Ownership Can Be Moved]]

---

#memory-models #rust #ownership
