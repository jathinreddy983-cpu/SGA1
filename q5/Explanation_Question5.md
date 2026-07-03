# Question 5 Explanation

- `lsblk`: This command listed the available block devices and their partitions. It helped identify storage devices such as `sda`, `sdb`, and `sdc`.
- `mount | head -5`: This command showed the currently mounted filesystems and their types. It confirmed that the system is using overlay and temporary filesystem mounts.
- `df -h`: This command displayed disk space usage for mounted filesystems. It showed that the root filesystem has significant used space while there is still free capacity available.
- `df -i`: This command reported inode usage. The output showed that inode usage was not near exhaustion, so the system did not appear to be limited by inode availability.
