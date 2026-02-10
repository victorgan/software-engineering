# Multiprocessing for CPU-bound

> <- Back to [[Python Concurrency]]

Python's `multiprocessing` module spawns separate processes, each with its own Python interpreter and GIL. This achieves true parallelism for CPU-bound work by sidestepping the GIL, at the cost of higher memory usage and inter-process communication overhead.

#concurrency #language-specific #python #multiprocessing
