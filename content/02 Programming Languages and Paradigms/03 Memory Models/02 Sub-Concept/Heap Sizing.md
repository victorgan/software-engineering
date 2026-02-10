# Heap Sizing

> <- Back to [[GC Tuning]]

Configuring the initial and maximum heap size (-Xms, -Xmx in JVM). Too small a heap causes frequent GC pauses; too large a heap wastes memory and can cause long individual pause times. The optimal size depends on the application's live object set and allocation rate.

#memory-models #gc #tuning #heap-size
