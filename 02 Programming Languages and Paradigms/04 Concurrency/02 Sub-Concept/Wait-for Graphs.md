# Wait-for Graphs

> <- Back to [[Deadlock Detection]]

A directed graph where nodes represent threads and edges represent "thread A is waiting for a resource held by thread B." A cycle in this graph indicates deadlock. The system periodically constructs and analyzes this graph to detect deadlock situations.

#concurrency #deadlock #detection #wait-for-graph
