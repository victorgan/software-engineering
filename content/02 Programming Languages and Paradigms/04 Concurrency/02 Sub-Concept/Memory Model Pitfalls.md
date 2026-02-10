# Memory Model Pitfalls

> <- Back to [[Double-Checked Locking]]

Double-checked locking is broken without proper memory ordering because the compiler or CPU may reorder the writes to the object fields and the reference publication. The reference may become visible to other threads before the object is fully constructed. Using volatile (Java) or atomic (C++) fixes this.

#concurrency #patterns #memory-model #pitfalls
