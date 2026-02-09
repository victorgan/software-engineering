# Limited Size

> <- Back to [[Stack Memory]]

Stack size is typically fixed (e.g., 1-8 MB per thread) and set at thread creation. Exceeding the stack limit causes a stack overflow, which is why recursive algorithms with deep recursion and large local allocations can be problematic.

#memory-models #stack #size-limit
