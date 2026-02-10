# Acquire-Release

> <- Back to [[Memory Ordering]]

An acquire operation (typically a load/lock) ensures that subsequent reads and writes are not reordered before it. A release operation (typically a store/unlock) ensures that preceding reads and writes are not reordered after it. Together they establish a happens-before relationship between threads.

#concurrency #lock-free #memory-ordering #acquire-release
