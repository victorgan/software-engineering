# Value Changes A to B to A

> <- Back to [[ABA Problem]]

A memory location holds value A. Thread 1 reads A and is preempted. Thread 2 changes the value to B, then back to A. Thread 1 resumes and CAS succeeds (seeing A), but the underlying data may have changed. This can corrupt lock-free data structures.

#concurrency #lock-free #aba
