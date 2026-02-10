# Facts and Rules

> <- Back to [[Declarative Rules]]

Facts are unconditional assertions about the world (e.g., `parent(tom, bob).`). Rules define relationships derived from other facts and rules (e.g., `grandparent(X, Z) :- parent(X, Y), parent(Y, Z).`). Together they form the knowledge base that the inference engine queries.

#programming-paradigms #logic #facts #rules
