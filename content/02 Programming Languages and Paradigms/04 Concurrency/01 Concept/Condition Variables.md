# Condition Variables

> <- Back to [[Synchronization Primitives]]

Synchronization primitives that allow threads to wait until a particular condition is met. A thread releases a mutex and sleeps on the condition variable; another thread signals/notifies when the condition changes, waking the waiting thread. Always used with a mutex and a predicate check loop.

## Key Properties

- [[Wait-Notify for Thread Coordination]]

---

#concurrency #synchronization #condition-variables
