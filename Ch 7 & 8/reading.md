# Chapter 7
**workload** - number of processes running in the system
**Turnaround Time** = completion time - time it arrived
 
# Performance metrics
- turnaround time
- fairness

**response time** = time of first run - time of arrival

# Types of Schedulers
- STCF/SJF shortest time to completion first or shortest job first
- RR Round Robin divides jobs and switches for each time segment
- MLFQ Multi-level Feedback Queue

# MLFQ
**Rule 1:** If Priority(A) > Priority(B), A runs
**Rule 2:** If Priority(A) = Priority(B), A & B run in RR
**Rule 3:** When a job enters the system, it is placed at the highest priority (the topmost queue).
**Rule 4:** Once a job uses up its time allotment at a given level (regardless of how many times it has given up on the CPU), its priority is reduced (it moves down one queue) 
**Rule 5:** After some time period S, move all jobs in the system to the topmost queue


