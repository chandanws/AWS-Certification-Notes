# RAID (Redundant Array of Independent Disks)

## Types of RAID
 - **RAID 0** - Striped, No Redundancy, Good performance
 - **RAID 1** - Mirrored, Redundancy
 - **RAID 5** - Good for reads, bad for writes, AWS does not recommend ever putting on RAID 5's on EBS
 - **RAID 10** - Stripped, Mirrored, Good Redundancy, Good Performance

**Best way to take a snapshot of a RAID array is to first shutdown the EC2 instance and then take the snapshot**