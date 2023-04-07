
# what are threads

A thread is a basic unit of CPU utilization; it  comprises a thread ID, a program counter (PC), a register set, and a stack.

# Multithreading models
1. **Many-to-One Model**
- maps many user-level threads to one kernel thread.
- Thread management is done by the thread library in user space, so it is efficient.
- The entire process will block if a thread makes a blocking system call.

2. **One-to-One Mode**
- maps each user thread to a kernel thread.
- more concurrency than the many-to-one model by allowing another thread to run when a thread makes a blocking system call.
- allows multiple threads to run in parallel on multiprocessors
- only drawback to this model is that creating a user thread requires creating the corresponding kernel thread, and a large number of kernel threads may burden the performance of a system.