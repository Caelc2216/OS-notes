# Chapter 41
**Fast File System (FFS)** improves performance by placing related files/metadata together

Directories are placed in cylinder groups with few directories and many free inodes

Files are placed in the same group as their inode

Files in the same directory are stored in the same group

For large data it is spread across multiple groups so there is still room for other files in the same directory


**amortization** reducing an overhead by doing more work per overhead paid
**parameterization** the technique of figuring out how many blocks to skip in order to avoid extra rotations

# Chapter 42
crash-consistency problem
# File System Checker (fsck)
slow
Performs checks on everything to make sure nothing is out of place it checks
- Superblock
- Free Blocks
- Inode state
- Inode links
- Duplicate pointers
- Bad blocks
- Directory checks

# Journaling (write-ahead logging)
writes a note to disk when updating so if power is disrupted or a crash occurs you can fix it
1. Journal write - write the contents of the transaction to the log
2. Journal commit - Write the transaction commit block TxE to the log
3. Checkpoint - Write the contents of the update to their final disk locations
4. Free - mark the transaction free in the journal by updating the journal superblock


# Metadata Journaling
1. Data Write
2. Journal metadata write
3. Journal Commit
4. Checkpoint metadata
5. Free

# Chapter 43
**Log-structured File System**
first buffers all updates (including metadata) in an inmemory segment, when the segment is full, it is written to disk in one long sequential transfer to an unused part of the disk.
- LFS never over-writes existing data, it always writes segments to free locations

**write buffering** before writing to the disk, LFS keeps track of updates in memory; when it has received a sufficient number of updates, it writes them to disk all at once

**Checkpoint region (CR)** contains pointers to the latest pieces of the inode map

**segment summary block** where information for each data block such as inode number and offset are stored. It is at the head of the segment

**shadow paging/copy-on-write** the approach of writing to an unused portion instead of overwriting
