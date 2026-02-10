# Uniform Interface

> <- Back to [[VFS (Virtual File System)]]

Applications use the same POSIX system calls regardless of the underlying file system. "Everything is a file" in Unix — regular files, devices, pipes, sockets, and even kernel interfaces (/proc, /sys) are accessed through the same file operations via VFS.

#operating-systems #file-systems
