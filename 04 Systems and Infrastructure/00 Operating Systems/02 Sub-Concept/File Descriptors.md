# File Descriptors

> <- Back to [[File System Concepts]]

Per-process integer handles that reference open files, sockets, pipes, and other I/O resources. File descriptors 0, 1, 2 are stdin, stdout, stderr by convention. The kernel maintains a file descriptor table per process and a system-wide open file table. Limited by ulimit settings.

#operating-systems #file-systems #io
