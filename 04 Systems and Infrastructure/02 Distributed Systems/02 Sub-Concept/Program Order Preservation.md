# Program Order Preservation

> <- Back to [[Sequential Consistency]]

Operations from a single process appear in the global order in the same sequence they were issued. If process P writes A then B, all nodes see A before B. Only the interleaving of operations from different processes may differ from real-time order.

#distributed-systems #consistency
