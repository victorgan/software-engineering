# Unused Type Parameters for Compile-time Safety

> <- Back to [[Phantom Types]]

Type parameters that exist only in the type signature, not in the runtime representation. For example, `Distance<Kilometers>` and `Distance<Miles>` have the same runtime structure but are incompatible types, preventing unit confusion at compile time with zero runtime cost.

#type-systems #phantom-types #safety
