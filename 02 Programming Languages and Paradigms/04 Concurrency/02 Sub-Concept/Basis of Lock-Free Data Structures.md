# Basis of Lock-Free Data Structures

> <- Back to [[Compare-and-Swap (CAS)]]

Lock-free data structures use CAS in a retry loop: read the current state, compute the new state, CAS to update. If another thread modified the state between read and CAS, the CAS fails and the operation retries with the new state. This ensures progress without locks.

#concurrency #lock-free #cas #data-structures
