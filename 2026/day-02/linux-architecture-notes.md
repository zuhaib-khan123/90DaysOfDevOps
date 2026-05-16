Kernel:

-> Core part of the operating system.
-> Directly interacts with hardware (CPU, RAM, devices).
-> Manages processes, memory, files, and system resources.

User Space:

-> Area where normal applications run.
-> Programs cannot directly access hardware.
-> Uses system calls to request services from the kernel.
-> Safer because app crashes usually don’t crash the whole OS.

init / systemd:

-> First process started after the kernel boots.
-> Has Process ID (PID) 1.
-> Starts and manages system services and background processes.
-> Handles boot process and service management.
-> systemd is the modern replacement for traditional init in most Linux distributions.
-> Examples of services managed: networking, SSH, databases.

-> Makes Linux boot faster.
-> Automatically keeps important services running

# Processes

* Running: 

Process is currently using CPU or ready to use CPU.
Either executing or waiting for CPU time.

*Sleeping:

Process is waiting for some event or resource.
Most common process state.

* Zombie:

Process finished execution but still has an entry in process table.
Happens when parent process has not collected child process status.

Called:

“Defunct” process.

# 5 Linux commands:
-> mkdir
-> touch file.txt
-> ls 
-> cat file.txt
-> cd 
