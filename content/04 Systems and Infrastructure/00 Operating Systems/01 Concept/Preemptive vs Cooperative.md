# Preemptive vs Cooperative

> <- Back to [[CPU Scheduling]]

Two fundamental approaches to CPU scheduling. Preemptive scheduling allows the OS to forcibly interrupt a running process to give CPU time to another, ensuring fairness. Cooperative scheduling relies on processes voluntarily yielding the CPU, risking starvation if a process misbehaves.

## Key Properties

- [[OS-Controlled Preemption]]
- [[Voluntary Yielding]]
- [[Time Quantum]]

## Related

- [[Scheduling Algorithms]] (most modern algorithms are preemptive)
- [[Green Threads and Fibers]] (typically use cooperative scheduling)

---

#operating-systems #scheduling
