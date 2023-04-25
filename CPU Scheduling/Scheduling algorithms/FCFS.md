# First-Come, First-Served Scheduling
- simplest CPU-scheduling algorithm
- FCFS scheduling algorithm is nonpreemptive.
-  the process that requests the CPU first is allocated the CPU first.
- The implementation of the FCFS policy is easily managed with a FIFO queue.
- When a process enters the ready queue, its PCB is linked onto the tail of the queue. When the CPU is free, it is allocated to the process at the head of the queue.
- The running process is then removed from the queue

**Disadvantage:-** 
1. the average waiting time under the FCFS policy is often quite long.
2. troublesome for interactive systems, where it is important that each process get a share of the CPU at regular intervals.