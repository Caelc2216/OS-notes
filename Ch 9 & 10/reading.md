# Chapter 9
**Proportional-Share Scheduler**
- tries to guarentee that each job gets a certain percentage of CPU time

**Lottery Scheduling**
each job is given a percentage that it will use the CPU and then it can give percentages to its subjobs. A random number is then chosen to run

**Stride Scheduling**
Each job in the system has a stride, which is inverse in proportion to the number of tickets it has. When a process runs you increment its pass counter by the stride value. The scheduler chooses to run the process that has the lowest pass value

**CFS Completely Fair Scheduler**
takes the sched-latency value and divides it by the number of jobs to get the time slice time. When a process is running it keeps track of its virtual runtime and when it is done it checks to see if any other processes have a virtual runtime less than the one just ran. It also uses min granularity to make sure the time slice doesn't get too small.

# Chapter 10
**MQMS Multi-queue multiprocessor scheduling**
multiple queues, one per CPU

**Cache coherence** 
When different CPUs share main memory. If CPU 1 fetches someting from memory and then modifies it. When CPU 2 fetches it it could fetch the old value instead of the new one

**bus snooping** 
each cache pays attention to memory updates by observing the bus that connects them to main memory. If a CPU sees this it will either invalidate or update its copy.

