# Lock-Free Stacks

> <- Back to [[Lock-Free Data Structures]]

Stack implementations where push and pop use CAS on the top pointer. The Treiber stack is the simplest lock-free stack: push CAS-es a new node onto the top, pop CAS-es the top to the next node. Susceptible to the ABA problem.

#concurrency #lock-free #stacks
