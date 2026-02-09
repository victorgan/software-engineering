# Causal Dependencies

> <- Back to [[Causal Consistency]]

The "happens-before" relationships between operations that form a directed acyclic graph. A depends on B if B was visible when A was performed. Systems track these dependencies to ensure replicas apply operations in an order that respects causality, even if network delays reorder messages.

#distributed-systems #consistency
