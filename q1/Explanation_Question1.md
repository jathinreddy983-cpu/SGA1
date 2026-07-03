# Question 1 Explanation

- `whoami`: This command was used to verify the active username in the terminal session. The output showed that the current user is `codespace`.
- `groups`: This command listed the groups associated with the current user account. The output confirmed membership in several Linux groups such as `codespace`, `docker`, `golang`, and `ssh`.
- `echo "$SHELL"`: This command displayed the default shell environment variable. The result confirmed that the shell in use is `/bin/bash`.
- `pwd`: This command showed the current working directory. The output confirmed that the terminal was currently located at `/`.
- `ls -ls`: This command listed the files and directories visible from the root directory. It helped verify the overall filesystem layout and permissions.
- `curl -s --max-time 10 https://youtube.com > /dev/null && echo "Network: youtube.com reachable"`: This command tested external network connectivity. The success message confirmed that the environment can reach youtube.com.
