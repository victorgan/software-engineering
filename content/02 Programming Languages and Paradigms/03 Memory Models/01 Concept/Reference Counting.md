# Reference Counting

> <- Back to [[Garbage Collection (GC)]]

Each object maintains a count of references pointing to it. When the count drops to zero, the object is immediately freed. Reference counting provides deterministic deallocation but cannot handle circular references without additional mechanisms.

## Key Properties

- [[Increment-Decrement Counts]]

## Related

- Used by Python, Swift, Objective-C

---

#memory-models #gc #reference-counting
