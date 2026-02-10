# Atomic Updates

> <- Back to [[Copy-on-Write]]

In copy-on-write file systems, the metadata pointer to data blocks is updated atomically. The old data remains intact until the new data is fully written and the pointer is switched. This means the file system is always in a consistent state, even during crashes.

#operating-systems #file-systems #reliability
