# Event Loop and Non-blocking I/O

> <- Back to [[Async-Await]]

An event loop polls for I/O readiness and dispatches callbacks or resumes suspended async functions. Non-blocking I/O means the thread is never idle waiting for I/O — it processes other tasks while waiting, enabling a single thread to handle thousands of concurrent connections.

#concurrency #models #async-await #event-loop
