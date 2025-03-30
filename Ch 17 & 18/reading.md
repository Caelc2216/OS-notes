# Chapter 17
**Best Fit** closest size to what you need
**Worst Fit** Returns largest chunk
**First Fit** First block that is big enough
**Next Fit** looks from where it was looking last
**binary buddy** only powers of 2 when freeing checks to see if buddy is being used if not it coalesces

# Chapter 18
**paging** choping the space into fixed size pieces
**page table** per process data structure that stores address translastions for each virtual page of the address space

Virtual Page Number = (Virtual Address & VPN Mask) >> Shift
Page Table Entry = Page Table Base + (VPN * sizeof(PTE))
offset = Virtual Address & Offset Mask
Physical Address = (Physical Frame Number << Shift) | offset