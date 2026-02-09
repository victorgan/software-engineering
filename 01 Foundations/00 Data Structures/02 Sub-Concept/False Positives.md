# False Positives

> ← Back to [[Bloom Filters]]

A Bloom filter may incorrectly report that an element is in the set when it is not. The false positive rate depends on the bit array size, number of hash functions, and number of inserted elements. Can be tuned by adjusting these parameters.

#property #probabilistic
