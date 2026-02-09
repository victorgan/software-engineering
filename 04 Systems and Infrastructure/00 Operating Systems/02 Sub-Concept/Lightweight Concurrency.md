# Lightweight Concurrency

> <- Back to [[Green Threads and Fibers]]

Green threads use very small stacks (e.g., 2-8 KB for goroutines vs 1-8 MB for OS threads), enabling millions of concurrent tasks on a single machine. This makes the "one thread per connection" model practical at massive scale.

#operating-systems #green-threads #concurrency
