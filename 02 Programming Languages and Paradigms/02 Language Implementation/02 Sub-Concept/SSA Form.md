# SSA Form

> <- Back to [[Intermediate Representation (IR)]]

Static Single Assignment form is an IR where every variable is assigned exactly once. Multiple assignments to the same variable are represented as different versioned names (x1, x2, x3), with phi-functions at control flow merge points. SSA simplifies many optimization algorithms and is used by LLVM, GCC, and most modern compilers.

#language-implementation #ir #ssa
