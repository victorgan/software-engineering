# Handling Circular References in Ref-counted Systems

> <- Back to [[Cycle Detection]]

When objects reference each other in a cycle, their reference counts never reach zero. Python uses a supplementary cycle-detecting collector that periodically traces objects to find unreachable cycles. Swift and Objective-C use weak references to break potential cycles manually.

#memory-models #gc #cycle-detection #circular
