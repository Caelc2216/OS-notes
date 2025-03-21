# Process creation in UNIX systems
- fork()
- exec()
- wait()

# fork()
used to create a new process. Creates an exact copy of the parent just with a different PID

# wait()
parent waits until child has executed

# exec()
transforms the current running process into a new process and doesn't return

# Questions
- Run through p2 program, if it doesn't return anything why does parent info still display?

# Handling Restrictions
User mode - restricted in what it can do, can't make I/O requests
Kernel mode - can do anything

when in User mode and needing to access restrincted info you perform a System call which allows the kernel to expose certain key pieces of functionality. This is what POSIX is. 

**trap instructions** - switch to kernal and raises privilege to kernel mode then when done 

**return-from-trap instructions** - return to user program and reduce priviledge back to user mode.

# Switching Processes
**Cooperative Approach** waits for a yeild or illegal action for OS to regain control

**Non-Cooperative Approach** uses a timer interrupt so after a certain amount of thime the interrupt handler in the OS takes controlos




