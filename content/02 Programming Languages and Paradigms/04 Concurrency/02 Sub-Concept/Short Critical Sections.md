# Short Critical Sections

> <- Back to [[Spinlocks]]

Spinlocks are appropriate only when the critical section is very brief (a few instructions). For longer critical sections, the CPU time wasted spinning exceeds the cost of putting the thread to sleep and waking it later, making a regular mutex more efficient.

#concurrency #synchronization #spinlocks #short
