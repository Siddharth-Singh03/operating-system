
# Round-Robin Scheduling
- similar to FCFS scheduling, but preemption is added to enable the system to switch between  processes
- A small unit of time, called a time quantum or time slice, is defined.
- The ready queue is treated as a circular queue.
- The CPU scheduler goes around the ready queue, allocating the CPU to each process for a time interval of up to 1 time quantum.
- New processes are added to the tail of the ready queue.
- The CPU scheduler picks the first process from the ready queue, sets a timer to interrupt after 1 time quantum, and dispatches the process.
- When the process have a CPU burst of
less than 1 time quantum. Then the process itself will release the CPU voluntarily. The scheduler will then proceed to the next process in the ready
queue.
- If the CPU burst of the currently running process is longer than 1 time quantum, the timer will go off and will cause an interrupt to the operating system.
**limitations:-**
1. The average waiting time under the RR policy is often long