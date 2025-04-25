# Chapter 44
flash chips are organized into banks or planes
banks are organized into blocks
blocks are organized into pages

In order to write to a page you first have to erase the entire block

# Operations
read(a page)
erase(a block)
program(a page)\

PAGE STATES
- Invalid
- Erased
- Valid

**disturbance** when bits in neighboring pages get flipped
**Flash Translation Layer (FTL)** takes read and write requests on logical blocks and turns them into low-level read, erase, and program commands on blocks and pages
**write amplification** the total write traffic issued to the flash chips by the FTL divided by the total write traffic issued by the client to the SSD
**wear leveling** having the FTL spread writes across the blocks to have them wear out at roughly the same time
**logging** the device appends the write to the next free spot in the currently-being-written-to-block

# Chapter 45
2 errors
- latent sector errors (LSE)
- block corruption

**LSE** when a disk sector has been damaged in some way

