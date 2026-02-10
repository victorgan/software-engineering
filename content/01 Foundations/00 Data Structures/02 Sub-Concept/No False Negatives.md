# No False Negatives

> ← Back to [[Bloom Filters]]

If a Bloom filter says an element is NOT in the set, it is guaranteed to be correct. This property makes Bloom filters useful as a first-pass filter — check the Bloom filter first, only do the expensive lookup if it says "maybe yes."

#property #probabilistic
