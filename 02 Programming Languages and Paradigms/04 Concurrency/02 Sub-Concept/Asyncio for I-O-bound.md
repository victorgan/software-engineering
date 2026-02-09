# Asyncio for I/O-bound

> <- Back to [[Python Concurrency]]

Python's `asyncio` module provides an event loop and async/await syntax for cooperative multitasking. Since I/O-bound tasks spend most of their time waiting, asyncio efficiently manages thousands of concurrent I/O operations on a single thread, unaffected by the GIL.

#concurrency #language-specific #python #asyncio
