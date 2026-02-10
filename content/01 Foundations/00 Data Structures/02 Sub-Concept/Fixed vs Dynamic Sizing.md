# Fixed vs Dynamic Sizing

> ← Back to [[Arrays]]

Static arrays have a fixed size set at allocation. Dynamic arrays (ArrayList, Vec, list) automatically resize by allocating a larger buffer and copying elements. Resize is O(n) but amortized O(1) per insertion.

#property #arrays
