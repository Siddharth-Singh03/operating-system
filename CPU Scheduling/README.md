
# CPU Scheduling

- In a system with a single CPU core, only one process can run at a time. Others must wait until the CPU’s core is free and can be rescheduled.
- The objective of multiprogramming is to have some process running at all times, to maximize CPU utilization

# Preemptive and Nonpreemptive Scheduling
- four circumstances for cpu scheduling decisions
1.  When a process switches from the running state to the waiting state (for example, as the result of an I/O request or an invocation of wait() for the termination of a child process)
2.  When a process switches from the running state to the ready state (for example, when an interrupt occurs)
3.  When a process switches from the waiting state to the ready state (for example, at completion of I/O)
4.  When a process terminates

- When scheduling takes place only under circumstances 1 and 4, we say that the scheduling scheme is nonpreemptive or cooperative.
- When scheduling takes place only under circumstances 2 and 3, we say that the scheduling scheme is preemptive.

# Dispatcher
- The dispatcher is the module that gives control of the CPU’s core to the process selected by the CPU scheduler
- This function involves the following:
1. Switching context from one process to another
2. Switching to user mode
3. Jumping to the proper location in the user program to resume that program 
