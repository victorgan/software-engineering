# Denormalization Tradeoff

> <- Back to [[Read vs Write Optimization]]

Storing redundant data to speed up reads. Denormalization eliminates joins and pre-computes aggregations, but requires updating multiple locations on writes. The consistency burden shifts from read time to write time.

#property #tradeoffs #denormalization
