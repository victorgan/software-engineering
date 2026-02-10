# Safety Without Runtime Overhead

> <- Back to [[Zero-Cost Abstractions]]

Rust's safety guarantees (ownership, borrowing, lifetimes) are enforced entirely at compile time and generate the same machine code as equivalent unsafe C/C++ code. There are no runtime checks, reference counting, or garbage collection pauses — safety is free.

#memory-models #rust #zero-cost #performance
