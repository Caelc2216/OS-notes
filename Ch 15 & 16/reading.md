# Chapter 15
**hardware-based address translation** translates virual address into physical address

physical address = virtual address + base

**base and bounds aka dynamic relocation**
base is the start of the address space and bounds is the end

**Memory management unit MMU** part of processor that helps with address translation, keeps trach of segments

**internal fragmentation** is the space between stack and heap that can be wasted

**External fragmentation** space that is free/on the free list

# Chapter 16
**stack** physical address = (virtual offset - max segment size) + base
**Heap** physical address = virual address + base

**Segmentation** having base and bounds for each segment
