# Cooperative Multitasking

> <- Back to [[Async-Await]]

Tasks voluntarily yield control at await points rather than being preempted by the scheduler. This cooperative model avoids the overhead of preemptive context switching but requires tasks to yield regularly — a long-running computation without await points can block the entire event loop.

#concurrency #models #async-await #cooperative
