# G1, ZGC, Shenandoah

> <- Back to [[Concurrent GC]]

Modern JVM garbage collectors designed for low latency. G1 (Garbage First) divides the heap into regions and collects the most garbage-filled first. ZGC and Shenandoah achieve sub-millisecond pauses through concurrent compaction using colored pointers and load barriers.

#memory-models #gc #concurrent #g1 #zgc #shenandoah
