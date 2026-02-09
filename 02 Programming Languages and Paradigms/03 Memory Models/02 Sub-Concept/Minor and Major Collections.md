# Minor and Major Collections

> <- Back to [[Generational GC]]

Minor collections run frequently and only scan the young generation, which is small and mostly garbage, resulting in fast pauses. Major (full) collections scan the entire heap including the old generation, are more thorough but cause longer pauses.

#memory-models #gc #generational #collections
