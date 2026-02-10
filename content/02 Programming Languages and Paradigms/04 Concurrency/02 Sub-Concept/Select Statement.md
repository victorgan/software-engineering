# Select Statement

> <- Back to [[Go Concurrency]]

Go's `select` statement multiplexes over multiple channel operations, executing whichever case is ready first. If multiple cases are ready, one is chosen randomly. A `default` case makes the select non-blocking. Similar to a switch statement but for channel operations.

#concurrency #language-specific #go #select
