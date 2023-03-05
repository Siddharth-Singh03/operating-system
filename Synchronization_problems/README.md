
# What is Synchronization?

- Synchronization in operating systems refers to the coordination and management of concurrent processes or threads to ensure that they execute in a predictable and orderly manner.
- When multiple processes or threads access shared resources like memory, files, or I/O devices, there can be issues such as race conditions, deadlock, and livelock. Synchronization mechanisms are used to prevent or resolve these issues.
- Synchronization is an essential concept in operating systems, especially in multi-tasking environments, where multiple processes or threads can run simultaneously. By synchronizing their access to shared resources, synchronization mechanisms ensure the integrity of data, prevent inconsistencies, and improve the performance and efficiency of the system


## Race condition

1. When more than one process is either running the same code or modifying the same memory or any shared data, there is a risk that the result or value of the shared data may be incorrect because all processes try to access and modify this shared resource. Thus, all the processes race to say that my result is correct. This condition is called the race condition. 

2. In the critical section, a race condition occurs when the end result of multiple thread executions varies depending on the sequence in which the threads execute.
## What is the Critical Section Problem?
- A part of code that can only be accessed by a single process at any moment is known as a critical section.
- This means that when a lot of programs want to access and change a single shared data, only one process will be allowed to change at any given moment. The other processes have to wait until the data is free to be used.
- The wait() function mainly handles the entry to the critical section, while the signal() function handles the exit from the critical section.
## Requirements of Synchronization
- **Mutual exclusion:** If a process is running in the critical section, no other process should be allowed to run in that section at that time.

- **Progress:** If no process is still in the critical section and other processes are waiting outside the critical section to execute, then any one of the threads must be permitted to enter the critical section. The decision of which process will enter the critical section will be taken by only those processes that are not executing in the remaining section.

- **No starvation:** Starvation means a process keeps waiting forever to access the critical section but never gets a chance. No starvation is also known as Bounded Waiting.

1. A process should not wait forever to enter inside the critical section.
2. When a process submits a request to access its critical section, there should be a limit or bound, which is the number of other processes that are allowed to access the critical section before it.
3. After this bound is reached, this process should be allowed to access the critical section.