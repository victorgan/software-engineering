# Traditional Model Requiring Synchronization

> <- Back to [[Threads & Shared Memory]]

The default concurrency model in most languages: OS threads share a single address space and communicate through shared variables. All access to shared mutable data must be synchronized with locks or atomics to prevent data races and ensure correctness.

#concurrency #models #shared-memory #synchronization
