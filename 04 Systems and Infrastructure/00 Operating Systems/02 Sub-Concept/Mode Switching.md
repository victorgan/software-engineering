# Mode Switching

> <- Back to [[Kernel vs User Space]]

The CPU transition between user mode and kernel mode during a system call. Involves saving user-space registers, switching to the kernel stack, executing the syscall handler, then restoring state and returning. Costs hundreds of nanoseconds — a key reason to minimize system calls in performance-critical code.

#operating-systems #memory #security #performance
