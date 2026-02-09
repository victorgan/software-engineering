# Process Termination

> <- Back to [[Process Lifecycle]]

A process ends when it calls exit, receives a fatal signal, or is killed by the OS. The kernel reclaims resources (memory, file descriptors) and notifies the parent process. Zombie processes occur when the parent hasn't read the exit status.

#operating-systems #processes #lifecycle
