
# CPU Scheduling

- In a system with a single CPU core, only one process can run at a time. Others must wait until the CPU’s core is free and can be rescheduled.
- The objective of multiprogramming is to have some process running at all times, to maximize CPU utilization

# Preemptive and Nonpreemptive Scheduling
- four circumstances for cpu scheduling decisions
1.  When a process switches from the running state to the waiting state (for example, as the result of an I/O request or an invocation of wait() for the termination of a child process)
2.  When a process switches from the running state to the ready state (for example, when an interrupt occurs)
3.  When a process switches from the waiting state to the ready state (for example, at completion of I/O)
4.  When a process terminates
