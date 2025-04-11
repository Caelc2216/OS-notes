# Chapter 32

# Non-Deadlock Bugs
**Atomicity violation** is when something is assumed to be atomic but isn't easy fix with locks
**order violation** when order matters but isnt enforced. Fixed with condition variables

# Deadlock Bugs
Ways to avoid
**Circular Wait** fix have an order to aquiring locks
**Hold and wait** aquire all locks needed at the same time
**No Preemption** using a trylock on the second lock and if it doestn't work it releases the first lock and tries again
**Mutual Exclusion** makes code not mutually exlusive using do while loop

**avoiding of deadlock via schedulint** if we know what locks each thread uses we can make sure to schedule in a way that doesn't cause deadlock