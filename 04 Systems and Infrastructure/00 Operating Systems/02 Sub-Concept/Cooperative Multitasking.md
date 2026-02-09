# Cooperative Multitasking

> <- Back to [[Coroutines]]

A concurrency model where tasks voluntarily give up the CPU rather than being forcibly preempted. Coroutines run until they hit a yield point, making execution order deterministic. This eliminates many race conditions but requires discipline to avoid blocking the event loop.

#operating-systems #coroutines #concurrency
