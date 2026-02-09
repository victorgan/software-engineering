# Circular Wait

> <- Back to [[Deadlock Conditions]]

A cycle of threads exists where each thread holds a resource that the next thread in the cycle is waiting for. Prevention: impose a total ordering on all resources and require threads to acquire them in order, breaking any potential cycle.

#concurrency #deadlock #circular-wait
