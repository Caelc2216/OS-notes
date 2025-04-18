# Chapter 38
RAID - Redundant Array of Inexpensive Disks

# Fault Models
**fail-stop** 2 stages working or failed. When it is in stage failed we assume it is permanently lost

Raids are evaluated by
- Capacity
- Reliability
- Performance

# RAID Levels
**RAID Level 0: Striping**
blocks of the array are placed across the disks in a round-robin fashion. The blocks in the same row are called a stripe. This is done to increase the performance through parallelism. All disks are utilized in parallel leading to shorter I/O requests, but if one disk fails there will be data loss.

S = sequential workload
S = Amount of Data/Time to access

R = random workload
R = Amount of Data/Time to access

**RAID Level 1: Mirroring**
Mirroring keeps a copy on another disk and therefore can handle failures.

**RAID Level 4: Saving Space With Parity**
Has a disk that stores the parity bits for each bit in the stripe

**RAID Level 5: Rotating Parity**
Identical to RAID-4 but it rotates the parity block for each stripe

# Chapter 39
open() is how to open a new file. It returns a file descriptor
fsync() writes all data not already written to disk
mv is how to rename a file from the command line
stat() or fstat() gives metadata of a file
chmod is how you can change the permissions of a file
