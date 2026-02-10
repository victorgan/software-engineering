# Lock-Free Queues

> <- Back to [[Lock-Free Data Structures]]

Queue implementations using CAS operations instead of locks. The Michael-Scott queue is a classic FIFO lock-free queue using CAS on head and tail pointers. Lock-free queues are essential for producer-consumer patterns in high-performance systems.

#concurrency #lock-free #queues
