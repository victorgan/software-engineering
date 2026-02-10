# Use-after-free

> <- Back to [[Common Memory Bugs]]

Accessing memory through a pointer after it has been freed. The memory may have been reallocated for a different purpose, causing data corruption, crashes, or exploitable security vulnerabilities. One of the most common sources of CVEs in C/C++ programs.

#memory-models #bugs #use-after-free
