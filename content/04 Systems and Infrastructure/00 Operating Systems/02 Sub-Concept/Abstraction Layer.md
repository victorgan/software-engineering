# Abstraction Layer

> <- Back to [[VFS (Virtual File System)]]

VFS defines a common set of operations (open, read, write, close, stat) that all file system implementations must provide. This abstraction lets applications work with any file system without modification, and allows the kernel to transparently switch between implementations.

#operating-systems #file-systems
