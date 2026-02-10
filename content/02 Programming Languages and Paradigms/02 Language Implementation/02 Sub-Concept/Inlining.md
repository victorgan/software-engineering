# Inlining

> <- Back to [[Optimization]]

Replacing a function call with the body of the called function. Inlining eliminates call overhead and enables further optimizations (like constant folding) within the expanded code. Compilers use heuristics to decide which functions are profitable to inline.

#language-implementation #optimization #inlining
