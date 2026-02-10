# G-Counter and PN-Counter

> <- Back to [[CRDTs]]

G-Counter (Grow-only Counter): each node maintains its own counter; the total is the sum of all nodes' counters. Only supports increment. PN-Counter: two G-Counters — one for increments, one for decrements. The value is the difference. Merge by taking the max of each node's counter.

#distributed-systems #crdts
