# Compile at Runtime Based on Hot Paths

> <- Back to [[Just-in-Time (JIT)]]

The JIT compiler profiles running code to identify frequently executed paths (hot paths) and compiles only those to native code. This enables speculative optimizations based on observed runtime behavior, such as inlining virtual method calls based on the most common receiver type.

#language-implementation #jit #hot-paths
