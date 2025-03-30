# Chapter 13
address space - contains the code segment, stack, and heap
**every generated address by a user program is a virtual adress**

VM (virtual memory) offers
- transparency - the program isn't aware of the fact that memory is virualized
- efficiency in time and space
- protection


# Chapter 14
2 types of memory
- stack aka automatic mem
- heap

malloc() is how you allocate space on the heap
free() - frees heap memory that is no longer in use
**dangling pointer** when a program frees up memory before it is finished using it

mmap() creates anonymous memory used for swap space