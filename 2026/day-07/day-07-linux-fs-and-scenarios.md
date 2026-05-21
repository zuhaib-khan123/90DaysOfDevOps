/ (root) - The starting point of everything
/home - User home directories
/root - Root user's home directory
/etc - Configuration files
/var/log - Log files (very important for DevOps!)
/tmp - Temporary files

-> Additional Directories :

/bin - Essential command binaries
/usr/bin - User command binaries
/opt - Optional/third-party application

Example Scenario: Check if a service is running

Question: How do you check if the 'nginx' service is running?
My Solution (Step by step):

Step 1: Check service status

systemctl status nginx
Why this command? It shows if the service is active, failed, or stopped

Step 2: If service is not found, list all services

systemctl list-units --type=service
Why this command? To see what services exist on the system

Step 3: Check if service is enabled on boot

systemctl is-enabled nginx
Why this command? To know if it will start automatically after reboot

What I learned: Always check status first, then investigate based on what you see.

Scenario 1: Service Not Starting

A web application service called 'myapp' failed to start after a server reboot.
What commands would you run to diagnose the issue?
Write at least 4 commands in order.

step1 : systemctl status myapp
why: to check status of service

step 2: journalctl -u myapp -n 50
why: it give the problem myapp is facing

step3: systemctl is-enabled myapp
why: check if myapp is enabled to start on boot

Scenario 2: 
Your manager reports that the application server is slow.
You SSH into the server. What commands would you run to identify
which process is using high CPU?

step 1: top 
why: give live running processes

step 2: htop
why : gives output in user-friendly/human readable format

step 3: ps aux --sort=-%cpu | head -10
why : gives list of processes using high cpu from first 10 lines

Scenario 3: Finding Service Logs

A developer asks: "Where are the logs for the 'docker' service?"
The service is managed by systemd.
What commands would you use?

step 1: journalctl -u ssh -n 50 
why : gives logs of last 50 lines

step 2: journalctl -u ssh -f
why : it gives docker real time logs


Scenario 4: File Permissions Issue

A script at /home/user/backup.sh is not executing.
When you run it: ./backup.sh
You get: "Permission denied"

What commands would you use to fix this?

Step 1: Check current permissions
Command: ls -l /home/user/backup.sh
Look for: -rw-r--r-- (notice no 'x' = not executable)
why : checks permissions focus on "x" executable or not

Step 2: Add execute permission
Command: chmod +x /home/user/backup.sh
why : add executable permission by chmod +x

Step 3: Verify it worked
Command: ls -l /home/user/backup.sh
Look for: -rwxr-xr-x (notice 'x' = executable)
why : To see changes are done or not

Step 4: Try running it
Command: ./backup.sh
why : To check is it executable or not