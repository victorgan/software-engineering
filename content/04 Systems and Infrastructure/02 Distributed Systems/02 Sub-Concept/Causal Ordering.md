# Causal Ordering

> <- Back to [[Causal Consistency]]

If operation A causally precedes operation B (B read a value written by A, or B was issued after A by the same process), then all nodes see A before B. This captures the intuitive notion that effects follow causes. Tracked using vector clocks or dependency tracking.

#distributed-systems #consistency
