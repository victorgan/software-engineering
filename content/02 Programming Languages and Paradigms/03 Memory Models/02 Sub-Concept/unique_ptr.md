# unique_ptr

> <- Back to [[Smart Pointers]]

A smart pointer that enforces exclusive ownership of a heap-allocated object. `unique_ptr` cannot be copied, only moved, ensuring exactly one owner at a time. When the `unique_ptr` is destroyed, the owned object is automatically deleted.

#memory-models #smart-pointers #unique-ptr
