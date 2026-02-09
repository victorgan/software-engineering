# Dangling Pointers

> <- Back to [[Common Memory Bugs]]

Pointers that reference memory that has been freed or is no longer valid. Dereferencing a dangling pointer causes undefined behavior. Common sources include returning pointers to local variables, freeing memory while other pointers still reference it, and iterator invalidation.

#memory-models #bugs #dangling-pointers
