# Zero-Copy IO

> <- Back to [[Memory-Mapped Files]]

Data transfer without copying between kernel and user space buffers. Memory-mapped files achieve this by sharing the kernel's page cache directly with the process. Other zero-copy mechanisms include sendfile() and splice(). Critical for high-performance networking and file serving.

#operating-systems #memory #io #performance
