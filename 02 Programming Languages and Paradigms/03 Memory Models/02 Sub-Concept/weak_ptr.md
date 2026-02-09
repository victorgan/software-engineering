# weak_ptr

> <- Back to [[Smart Pointers]]

A non-owning reference to an object managed by `shared_ptr`. `weak_ptr` does not prevent deallocation and must be converted to a `shared_ptr` to access the object. Used to break circular references between `shared_ptr` instances.

#memory-models #smart-pointers #weak-ptr
