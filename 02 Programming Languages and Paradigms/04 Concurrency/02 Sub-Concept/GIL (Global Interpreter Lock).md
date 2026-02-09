# GIL (Global Interpreter Lock)

> <- Back to [[Python Concurrency]]

A mutex in CPython that allows only one thread to execute Python bytecode at a time. The GIL simplifies the interpreter's implementation and C extension development but prevents true parallelism for CPU-bound Python code on multi-core systems.

#concurrency #language-specific #python #gil
