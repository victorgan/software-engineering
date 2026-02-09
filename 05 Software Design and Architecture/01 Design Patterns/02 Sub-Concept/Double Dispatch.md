# Double Dispatch

> <- Back to [[Visitor]]

A technique where the method called depends on the runtime types of two objects (the element and the visitor). The element accepts a visitor and calls back the visitor's specific visit method, enabling type-safe operation dispatch without type checks.

#property #visitor #double-dispatch
