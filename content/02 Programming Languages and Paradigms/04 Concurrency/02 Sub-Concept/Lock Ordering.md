# Lock Ordering

> <- Back to [[Deadlock Prevention]]

Assigning a global order to all locks and requiring every thread to acquire locks in that order. This eliminates circular wait (one of the four deadlock conditions), preventing deadlock by construction. The challenge is maintaining consistent ordering across a large codebase.

#concurrency #deadlock #prevention #lock-ordering
