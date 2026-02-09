# Structural Sharing

> ← Back to [[Persistent Data Structures]]

New versions share unchanged portions with previous versions instead of copying everything. A tree update only copies nodes on the path from root to the modified leaf — O(log n) nodes — while sharing the rest. Keeps persistent structures space-efficient.

#property #functional
