# Compile-time Tracking of Reference Validity

> <- Back to [[Lifetimes]]

The Rust compiler's borrow checker tracks the lifetime of every reference to ensure it does not outlive the data it points to. Lifetime annotations (like `'a`) help the compiler reason about reference validity across function boundaries, preventing dangling references without runtime checks.

#memory-models #rust #lifetimes #borrow-checker
