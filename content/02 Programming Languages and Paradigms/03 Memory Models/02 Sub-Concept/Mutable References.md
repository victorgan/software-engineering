# Mutable References

> <- Back to [[Borrowing]]

Exclusive references (`&mut T`) that allow read-write access to data. Only one mutable reference can exist at a time, and no immutable references can coexist with it. This exclusivity prevents data races at compile time.

#memory-models #rust #borrowing #mutable
