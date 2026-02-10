# Increment-Decrement Counts

> <- Back to [[Reference Counting]]

When a new reference to an object is created, the count is incremented. When a reference is removed or goes out of scope, the count is decremented. When the count reaches zero, the object is immediately deallocated, providing deterministic destruction timing.

#memory-models #gc #reference-counting #counts
