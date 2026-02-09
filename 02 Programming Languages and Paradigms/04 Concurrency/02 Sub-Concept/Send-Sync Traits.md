# Send-Sync Traits

> <- Back to [[Rust Concurrency]]

`Send` marks types that can be safely transferred between threads. `Sync` marks types that can be safely shared between threads via references. These marker traits are automatically derived by the compiler, encoding thread safety in the type system.

#concurrency #language-specific #rust #send #sync
