# Concurrent Operations

> <- Back to [[Causal Consistency]]

Operations with no causal relationship (neither knows about the other) are concurrent and may be ordered differently by different nodes. This is the key relaxation that makes causal consistency weaker than sequential consistency but allows better performance since concurrent operations need not be globally ordered.

#distributed-systems #consistency
