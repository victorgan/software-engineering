# Linearizability

> <- Back to [[Strong Consistency]]

The strongest single-object consistency model. Every operation appears to take effect atomically at some point between its invocation and completion. This means the system behaves as if operations are executed on a single copy in real-time order. Used by Google Spanner with TrueTime.

#distributed-systems #consistency
