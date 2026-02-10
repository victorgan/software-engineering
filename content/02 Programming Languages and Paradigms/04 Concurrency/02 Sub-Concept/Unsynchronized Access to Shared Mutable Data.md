# Unsynchronized Access to Shared Mutable Data

> <- Back to [[Data Races]]

When two or more threads access the same memory location without synchronization and at least one is a write, the result is a data race. In C/C++ and Rust, data races are undefined behavior. Rust prevents them at compile time through the ownership system.

#concurrency #hazards #data-races #unsynchronized
