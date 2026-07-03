# Question 2 Explanation

- `mkdir -p secure_workspace/{docs,src,logs}`: This command created the required directory structure for the project workspace. It organized files into documentation, source, and logs folders.
- `touch secure_workspace/docs/plan.txt secure_workspace/src/app.txt secure_workspace/logs/activity.log`: This command created the sample project files inside their respective folders. These files represent the data that needs to be protected.
- `ls -ld secure_workspace secure_workspace/*`: This command displayed the directory permissions and confirmed the workspace layout. It showed that the directories were initially created with broad access.
- `chmod 750 secure_workspace` and `chmod 750 secure_workspace/docs secure_workspace/src secure_workspace/logs`: These commands restricted access to the workspace directories so that only the owner and group could traverse them. This helps prevent unauthorized users from reading sensitive project files.
- `chmod 640 secure_workspace/docs/plan.txt secure_workspace/src/app.txt secure_workspace/logs/activity.log`: This command set the project files to be readable by the owner and group only. The attempt for activity.log failed because the file name was typed incorrectly.
- `umask`: This command showed the default permission mask used when new files and directories are created. With `0022`, new files default to `644` and directories to `755` unless changed manually.
