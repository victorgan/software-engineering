# Ownership Prevents Data Races

> <- Back to [[Rust Concurrency]]

Rust's ownership and borrowing rules prevent data races at compile time. You cannot have mutable and shared access simultaneously, which is precisely the condition for a data race. This makes "fearless concurrency" possible — if it compiles, it is free of data races.

#concurrency #language-specific #rust #ownership
