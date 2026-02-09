# Lock-Free Hash Maps

> <- Back to [[Lock-Free Data Structures]]

Hash map implementations that avoid locks, typically using CAS for bucket updates and techniques like split-ordered lists or lock-free linked lists per bucket. Java's ConcurrentHashMap uses lock striping (not fully lock-free) for practical concurrent access.

#concurrency #lock-free #hash-maps
