# Immutable References

> <- Back to [[Borrowing]]

Shared references (`&T`) that allow read-only access to data. Multiple immutable references can exist simultaneously, enabling safe concurrent reads. While an immutable borrow is active, the data cannot be modified.

#memory-models #rust #borrowing #immutable
