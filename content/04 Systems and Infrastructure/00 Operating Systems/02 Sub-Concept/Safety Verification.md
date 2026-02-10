# Safety Verification

> <- Back to [[eBPF]]

The eBPF verifier statically analyzes programs before loading them into the kernel, ensuring they terminate, do not access invalid memory, and cannot crash the kernel. This safety guarantee is what makes it possible to run user-provided code in kernel space without risk.

#operating-systems #linux #security
