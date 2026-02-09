# Privilege Levels

> <- Back to [[Kernel vs User Space]]

Hardware-enforced protection rings (Ring 0 for kernel, Ring 3 for user space on x86). Kernel mode code can execute any instruction and access all memory; user mode code is restricted. Attempting privileged operations from user space triggers a fault, enforced by the CPU.

#operating-systems #memory #security
