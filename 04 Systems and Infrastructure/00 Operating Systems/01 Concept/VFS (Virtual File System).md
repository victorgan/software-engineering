# VFS (Virtual File System)

> <- Back to [[File Systems]]

An abstraction layer in the kernel that provides a uniform interface for different file system implementations. Applications use the same system calls (open, read, write) regardless of whether the underlying file system is ext4, NFS, procfs, or tmpfs. Mount points connect different file systems into a unified directory tree.

## Key Properties

- [[Abstraction Layer]]
- [[Mount Points]]
- [[Uniform Interface]]

## Related

- [[File System Concepts]] (VFS abstracts over these)
- [[Distributed File Systems]] (accessed through VFS)

---

#operating-systems #file-systems
