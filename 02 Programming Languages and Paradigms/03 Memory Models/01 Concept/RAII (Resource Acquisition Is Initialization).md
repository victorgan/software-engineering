# RAII (Resource Acquisition Is Initialization)

> <- Back to [[Manual Memory Management]]

A C++ idiom where resource lifetime is tied to object lifetime. Resources (memory, file handles, locks) are acquired in constructors and released in destructors, ensuring deterministic cleanup when objects go out of scope, even in the presence of exceptions.

## Key Properties

- [[C++ Destructors]]
- [[Deterministic Cleanup]]

---

#memory-models #manual-memory #raii
