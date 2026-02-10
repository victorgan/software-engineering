# Each Value Has One Owner

> <- Back to [[Ownership Rules]]

In Rust, every value has exactly one variable that owns it. When the owner goes out of scope, the value is automatically dropped (freed). This single-ownership rule eliminates the need for garbage collection while preventing double-free bugs.

#memory-models #rust #ownership #single-owner
