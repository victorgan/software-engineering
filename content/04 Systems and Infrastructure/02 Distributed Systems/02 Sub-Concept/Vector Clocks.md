# Vector Clocks

> <- Back to [[Distributed Time]]

An extension of Lamport clocks that can determine if two events are causally related or concurrent. Each node maintains a vector of counters (one per node). If all entries in V(A) are less than or equal to V(B), then A causally precedes B. Used by DynamoDB and Riak for conflict detection.

#distributed-systems #time
