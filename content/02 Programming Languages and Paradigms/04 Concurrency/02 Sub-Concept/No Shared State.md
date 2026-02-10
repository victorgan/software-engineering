# No Shared State

> <- Back to [[Actor Model]]

Actors never share mutable state directly. All communication happens through immutable messages. This eliminates data races by design — no locks are needed because no memory is shared. Each actor is a single-threaded unit of concurrency.

#concurrency #models #actors #no-sharing
