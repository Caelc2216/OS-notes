# Chapter 28
**spin-waiting** endlessly checks the value of a flag

# Hardware Support
**test and set** tests the old value and sets the new one simultaneously.
**compare and swap** tests if value is equal to expected and if it is updates with the new value
**Load Linked and Store Conditional** Loads the value and if the value hasn't changed since it's been loaded StoreConditional will update it to the new value passed in
**fetch and add** gets instruction and adds 1 to it

# OS Support
the OS uses a queue to make sure that no processes are starving. 

# Chapter 29
**approximate counters** each thread has a local counter that it increments until it gets to the threshold S at which point it adds the value to the global counter and resets the local counter to 0.
**hand over hand locking** You have locks for each node in a linked list

