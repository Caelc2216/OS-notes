# Chapter 26
**multi-theading** - program has more than one point of execution. Like a separate process but it shares the same address space/data

OS performs similar context switches when switching threads

threads have multiple stacks, one per thread

# Reasons  to use threads
1. Parallelism
2. Efficient during IO

pthread_join() waits for a particular thread to complete

**race condition/data race** when the results depend on the timing of the code's execution

**critical section** a piece of code that accesses a shared variable and must not be concurrently executed by more than one thread

**mutual exclusion** if one thread is running within the critical section the others will be prevented from running in that section

**atomic** "all or nothing"

# Chapter 27
To protect critical sections you can use locks to ensure only one thread can use the critical section at a time