# Ownership Can Be Moved

> <- Back to [[Ownership Rules]]

Ownership of a value can be transferred from one variable to another through move semantics. After a move, the original variable is no longer valid, preventing use-after-move bugs. Types implementing the Copy trait are implicitly duplicated instead of moved.

#memory-models #rust #ownership #move
