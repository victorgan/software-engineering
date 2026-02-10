# Trace Reachable Objects

> <- Back to [[Mark-and-Sweep]]

The mark phase starts from root references (stack variables, global variables, registers) and traverses all object references, marking each reachable object as alive. Any object not reached during this traversal is considered garbage.

#memory-models #gc #mark #tracing
