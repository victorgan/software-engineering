# Atomic Broadcast

> <- Back to [[Zab]]

A communication primitive that delivers messages to all nodes in the same total order. If any correct node delivers message A before B, all correct nodes deliver A before B. Zab implements atomic broadcast to ensure all ZooKeeper replicas apply state changes in identical order.

#distributed-systems #consensus
