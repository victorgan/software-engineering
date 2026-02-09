# Hard and Soft Links

> <- Back to [[File System Concepts]]

Hard links are additional directory entries pointing to the same inode — the file persists until all hard links are removed. Soft links (symlinks) are separate files containing a path to the target — they can cross file system boundaries and can become dangling if the target is deleted.

#operating-systems #file-systems
