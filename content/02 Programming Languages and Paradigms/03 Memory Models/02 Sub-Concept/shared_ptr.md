# shared_ptr

> <- Back to [[Smart Pointers]]

A reference-counted smart pointer that allows multiple owners of the same heap object. The object is deleted when the last `shared_ptr` to it is destroyed. Thread-safe reference counting adds overhead but enables shared ownership patterns.

#memory-models #smart-pointers #shared-ptr
