# Thread Stack

> <- Back to [[Thread]]

Each thread has its own stack for local variables and function call frames, while sharing the heap with other threads in the same process. Stack size is typically fixed (e.g., 1-8 MB on Linux) and stack overflow occurs if exceeded.

#operating-systems #threads #memory
