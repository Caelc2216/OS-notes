# Chapter 40
vsfs - very simple file system
**data region** the region of the disk where we store user data
**bitmap** structure used to indicate whether the corresponding object/block is free (0) or in use (1)
**superblock** contains info about the file system such as how many inodes, data blocks, where the inode table starts


# Inode (Index Node)
inode is the low-level name of the file
**extend** a disk pointer plus a length to read data
multi-level index
- direct pointers
- indirect pointers
- double indirect pointers
- triple indirect pointers

# Access Path
**dynamic partitioning** integrate virtual memory pages and file system pages into a **unified page cache**
**write buffering** delaying writes, the system can **batch** I/O requests to save from doing multiple I/O requests
