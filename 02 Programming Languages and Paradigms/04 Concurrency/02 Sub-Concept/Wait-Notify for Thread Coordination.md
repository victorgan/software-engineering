# Wait-Notify for Thread Coordination

> <- Back to [[Condition Variables]]

A thread waits on a condition variable when a condition is not met, atomically releasing the associated mutex and sleeping. Another thread signals/notifies the condition variable when the condition changes, waking the waiting thread which re-acquires the mutex. Always used in a while-loop to handle spurious wakeups.

#concurrency #synchronization #condition-variables #wait-notify
