# Bounded Buffer

> <- Back to [[Producer-Consumer]]

A fixed-size buffer between producers and consumers. When full, producers block until space is available; when empty, consumers block until data arrives. The bounded size provides natural backpressure, preventing producers from overwhelming the system's memory.

#concurrency #patterns #producer-consumer #buffer
