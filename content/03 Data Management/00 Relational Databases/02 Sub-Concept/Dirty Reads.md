# Dirty Reads

> <- Back to [[Concurrency Phenomena]]

Reading data that has been modified by another transaction but not yet committed. If that transaction rolls back, the read data was never valid.

#relational-databases #transactions #concurrency-phenomena
