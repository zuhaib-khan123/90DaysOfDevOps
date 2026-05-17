# Process management commands

| Command               | Use                             |
| --------------------- | ------------------------------- |
| `ps`                  | Show running processes          |
| `ps aux`              | Detailed list of all processes  |
| `top`                 | Real-time process monitoring    |
| `htop`                | Interactive/human-readle process       viewer      |
| `pidof process_name`  | Find process ID                 |
| `pgrep process_name`  | Search process by name          |
| `kill PID`            | Stop a process                  |
| `kill -9 PID`         | Force kill process              |
| `pkill process_name`  | Kill by process name            |
| `jobs`                | Show background jobs            |
| `nice -n 10 command`  | Start process with priority     |
| `renice priority PID` | Change running process priority |
| `free -h`             | Show memory usage               |
| `uptime`              | System uptime and load          |

# File System commands

| Command                    | Use                        |
| -------------------------- | -------------------------- |
| `pwd`                      | Show current directory     |
| `ls`                       | List files                 |
| `ls -la`                   | Detailed hidden files list |
| `cd directory`             | Change directory           |
| `mkdir folder`             | Create folder              |
| `rmdir folder`             | Remove empty folder        |
| `rm file`                  | Delete file                |
| `rm -rf folder`            | Delete folder recursively  |
| `cp source dest`           | Copy files                 |
| `mv source dest`           | Move/rename files          |
| `touch file.txt`           | Create empty file          |
| `cat file.txt`             | View file content          |
| `less file.txt`            | Read large files           |
| `head file.txt`            | First 10 lines             |
| `tail file.txt`            | Last 10 lines              |
| `tail -f log.txt`          | Live log monitoring        
| `du -sh folder`            | Folder size                |
| `df -h`                    | Disk space usage           |
| `chmod 755 file`           | Change permissions         |
| `chown user:user file`     | Change ownership           |
        
# Networking commands

ip a	 -> Show IP addresses
ifconfig ->	Network interface info
ping google.com	-> Test connectivity
traceroute google.com  ->	Trace network path
netstat -tulnp  ->	Show listening ports
