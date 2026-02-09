# State Save and Restore

> <- Back to [[Context Switching]]

The kernel saves the current process's registers, program counter, and stack pointer to its Process Control Block (PCB), then loads the next process's state. This is the core mechanism that enables multitasking on a single CPU.

#operating-systems #context-switching
