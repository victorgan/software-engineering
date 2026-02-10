# CAS Doesn't Detect Intermediate Change

> <- Back to [[ABA Problem]]

CAS only compares the current value with the expected value — it cannot detect that the value changed and changed back. Solutions include tagged pointers (appending a version counter that increments on every change), hazard pointers, and epoch-based reclamation.

#concurrency #lock-free #aba #detection
