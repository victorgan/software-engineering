# Explicit Allocation and Deallocation

> <- Back to [[malloc-free]]

The programmer explicitly requests memory with `malloc()` (or `calloc()`, `realloc()`) and releases it with `free()`. This provides maximum control but places full responsibility on the programmer to avoid leaks, double-frees, and use-after-free bugs.

#memory-models #manual-memory #malloc #free
