
# Shortest-Job-First Scheduling
- This algorithm associates with each process the length of the process’s next CPU burst. 
- The SJF algorithm can be either preemptive or nonpreemptive.
- When the CPU is available, it is assigned to the process that has the smallest next CPU burst
- t. If the next CPU bursts of two processes are the same, FCFS scheduling is used to break the  tie.
**limitations:-**

1. it cannot be implemented at the level of CPU scheduling, as there is no way to know the length of the next CPU burst.
