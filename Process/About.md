
# Process

A process is a program in execution.

# Process Management

- Process management invloves managing the execution of multiple processes or tasks within the system. 
- process management involves managing the creation, scheduling, synchronization, and termination of these processes.

- The key functions of process management in an operating system include:

1. **Process creation:** The process manager creates new processes as required by the system or user requests.

2. **Process scheduling:** The process manager decides which process to execute next and allocates CPU time accordingly.

3. **Process synchronization:** The process manager ensures that multiple processes do not interfere with each other and that they can communicate and synchronize as needed.

4. **Process termination:** The process manager terminates processes that have completed their tasks or have exceeded their allocated resources.

5. **Memory management:** The process manager ensures that each process has access to the memory it needs and that memory is allocated efficiently.

6. **Resource allocation:** The process manager allocates system resources, such as CPU time and input/output devices, to each process according to their needs.

# Process State

- **New:** The process is being created.
- **Running:** Instructions are being executed.
- **Waiting:** The process is waiting for some event to occur (such as an I/O completion or reception of a signal).
- **Ready:** The process is waiting to be assigned to a processor.
- **Terminated:** The process has finished execution.

# Process Control Block
- Each process is represented in the operating system by a process control
block
- It contains many pieces of information associated with a specific process, including
1. **Process state:** The state may be new, ready, running, waiting, halted, and so on.
2. **Program counter:** The counter indicates the address of the next instruction to be executed for this process.
3. **CPU registers:** The registers vary in number and type, depending on the computer architecture. They include accumulators, index registers, stack pointers, and general-purpose registers, plus any condition-code information. Along with the program counter, this state information must be saved when an interrupt occurs, to allow the process to be continued correctly afterward when it is rescheduled to run.
4. **CPU-scheduling information:** This information includes a process priority, pointers to scheduling queues, and any other scheduling parameters.
5. **Memory-management information:** This information may include such items as the value of the base and limit registers and the page tables, or the segment tables, depending on the memory system used by the operating system.
6. **Accounting information:** This information includes the amount of CPU
and real time used, time limits, account numbers, job or process numbers,
and so on.
7. **I/O status information:** This information includes the list of I/O devices
allocated to the process, a list of open files, and so on

# Process Scheduling 
- objective of multiprogramming is to have some process running at all times so as to maximize CPU utilization.
- the process scheduler selects an available process (possibly from a set of several available processes) for program execution on a core.
- The number of processes currently in memory is known as the degree of multiprogramming.
- In general, most processes can be described as either I/O bound or CPU bound. An I/O-bound process is one that spends more of its time doing I/O than it spends doing computations. A CPU-bound process, in contrast, generates I/O requests
infrequently, using more of its time doing computations

# Context Switching 
- interrupts cause the operating system to change a CPU core from its current task and to run a kernel routine.
- When an interrupt occurs, the system needs to save the current context of the process running on the CPU core so that it can restore that context when its processing is done, essentially suspending the process and then resuming it.
-  Generically, we perform a state save of the current state of the CPU core, be it in kernel or user mode, and then a state restore to resume operations.
-  Switching the CPU core to another process requires performing a state save of the current process and a state restore of a different process. This task is known as a context switch.

# Interprocess communication
- A process is **independent** if it does not share data with any other processes executing in the system. A process is **cooperating** if it can affect or be affected by the other processes executing in the system.
- There are two fundamental models of interprocess communication: shared memory and message passing.

