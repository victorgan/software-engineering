# Context Switching

> <- Back to [[Processes and Threads]]

Saving and restoring the state (registers, program counter, memory mappings) of a process or thread so that execution can resume later. Context switches have CPU overhead and are more expensive between processes than between threads within the same process.

## Key Properties

- [[State Save and Restore]]
- [[CPU Overhead]]
- [[TLB Flush]]

## Related

- [[Process]] (cross-process switches are more expensive)
- [[Thread]] (thread switches are cheaper — shared address space)
- [[CPU Scheduling]] (scheduling decisions trigger context switches)

---

#operating-systems #processes #performance
