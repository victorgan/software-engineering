# Shared Memory IPC

> <- Back to [[Inter-Process Communication (IPC)]]

A region of memory mapped into multiple processes' address spaces, enabling the fastest IPC since data does not need to be copied between kernel and user space. Requires synchronization (semaphores, mutexes) to avoid race conditions.

#operating-systems #ipc #memory
