# Young and Old Generations

> <- Back to [[Generational GC]]

Memory is divided into generations based on object age. The young generation holds newly created objects (most die quickly). Objects that survive multiple young-gen collections are promoted to the old generation, which is collected less frequently.

#memory-models #gc #generational #generations
