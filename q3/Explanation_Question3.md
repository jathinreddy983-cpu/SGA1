# Question 3 Explanation

- `echo "Linux link test file" > original.txt`: This command created the original file that would be used in the link experiment.
- `ln original.txt hardlink.txt`: This created a hard link, which points to the same inode as the original file. Both names refer to the same underlying data.
- `ln -s original.txt symlink.txt`: This created a symbolic link, which is a separate entry that contains the path to the target file.
- `ls -li` and `stat`: These commands showed the inode numbers and link counts, confirming that the hard link shares the same inode while the symbolic link has a different inode.
- `rm original.txt`: Removing the original filename did not affect the hard link, but it broke the symbolic link because its target no longer existed.
