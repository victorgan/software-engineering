# Double-free

> <- Back to [[Common Memory Bugs]]

Calling `free()` on the same pointer twice. This corrupts the memory allocator's internal data structures, potentially leading to crashes, heap corruption, or exploitable vulnerabilities where an attacker can control subsequent allocations.

#memory-models #bugs #double-free
