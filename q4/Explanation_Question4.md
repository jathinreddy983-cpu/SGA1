# Question 4 Explanation

- `echo "sample log line" > app.log`: This command created a sample log file that could be investigated as part of file access and I/O analysis.
- `lsof | head -n 20`: This showed open files and the processes that were using them. It helped identify active file descriptors in the current environment.
- `exec 3<app.log`: This opened the log file for reading using file descriptor 3. It demonstrated how shells manage file access using descriptors.
- `lsof -p $$ | grep app.log` and `ls -l /proc/$$/fd`: These commands confirmed that the shell process had the file open and exposed the file descriptor information.
- `ls -l > stdout.txt`, `ls /not_a_real_path 2> stderr.txt`, and `(ls -l && ls /not_a_real_path) > combined.txt 2>&1`: These commands demonstrated standard output redirection, standard error redirection, and the combination of both streams into one file.
- `ulimit -a`: This displayed the current shell resource limits, showing the environment’s constraints for processes and file handling.
