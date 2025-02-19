
### how load avg is calculated in linux 
In Linux, load average represents the system's workload over a period of time. It is calculated based on the number of processes in the system that are either:

Using the CPU (actively running)
Waiting for CPU time (in a runnable state but not currently being executed)
Waiting for I/O (blocked on some form of input/output operation)
The load average is typically displayed as three numbers, representing the system load over the last 1, 5, and 15 minutes.

The calculation of the load average involves a weighted moving average. Here's how it works:

Formula:
The load average for each time period (1, 5, 15 minutes) is calculated based on the following formula:

pgsql
Copy
Load Average(t) = Load Average(t-1) * e^(-1/τ) + Current Load * (1 - e^(-1/τ))
Where:

t is the current time period (1, 5, or 15 minutes).
τ is a time constant (specific for each period: 1 minute has a different τ than 5 or 15 minutes).
Load Average(t-1) is the previous load average value for the corresponding period.
Current Load is the current number of processes that are either actively running or waiting to be run.
Detailed Steps:
Sampling: The system periodically samples the number of processes in different states (running, waiting for CPU, waiting for I/O).
Decay over Time: The load averages decay over time using the exponential smoothing formula. Shorter periods (like 1 minute) decay more quickly than longer periods (like 15 minutes), giving a more current reflection of the system load.
Weighting: The shorter-term load average is weighted more heavily compared to the longer-term ones.
Example:
1-minute load average: Reflects the most recent system activity. It changes more rapidly.
5-minute load average: Gives an average of the system’s performance over the last 5 minutes.
15-minute load average: A slower-moving indicator of system load that smooths out short spikes and reflects longer-term trends.
Practical Interpretation:
Load Average < CPU Cores: The system is under-utilized. If your machine has 4 cores, a load average of 2.0 means there’s plenty of idle time.
Load Average ≈ CPU Cores: The system is fully utilized but not overloaded. For 4 cores, a load average of 4.0 means all CPU cores are working efficiently.
Load Average > CPU Cores: The system is overloaded. A load average of 5.0 on a 4-core machine means there are processes waiting for CPU time.
The load average can be checked using commands like uptime, top, or cat /proc/loadavg.

### what is swap space in linux

Swap space in Linux is a type of virtual memory that is used when the physical RAM (Random Access Memory) becomes full. It allows the system to move less frequently used data from RAM to a designated area on the disk, freeing up space in RAM for more urgent tasks.

Swap space is essentially an extension of the system's physical memory, allowing the operating system to continue functioning smoothly even when there is not enough RAM to store all running processes and data.

How Swap Space Works:
When RAM is Full: When the system’s RAM is fully utilized, and new processes or data need to be loaded into memory, the kernel moves less active parts of memory (pages of processes) to the swap space to make room in RAM.

Virtual Memory Management: This is part of the operating system's virtual memory management. The system swaps out data that is not currently in use to the swap space, effectively creating the illusion of more physical memory than is actually available.

Swapping In and Out: The data moved to swap space is swapped back into RAM when needed. This process is called "swapping in" (when the data is moved back to RAM) and "swapping out" (when the data is moved to swap space).

Types of Swap Space:
Swap Partition: A dedicated disk partition formatted as swap space. It is the most common way of setting up swap space on Linux.

Swap File: A regular file on an existing filesystem that is used as swap space. This can be created and managed easily without the need to repartition the disk.

Swap Space Characteristics:
Slower Than RAM: Disk storage is much slower than RAM, so using swap space can significantly degrade system performance if the system has to swap data in and out frequently. However, swap space is much larger in capacity than physical RAM, so it provides a safety net.

Threshold for Swapping: Modern Linux systems generally try to avoid swapping unless absolutely necessary. The kernel has a swapiness parameter that defines how aggressively the system uses swap space. The default value is typically 60, which means the kernel will start using swap space when around 60% of the RAM is full.

When Is Swap Space Used?
When System RAM is Exhausted: If your system runs out of available RAM for processes, swap space will be used.

To Improve System Stability: If too many processes are running simultaneously, swap space ensures that the system doesn't crash due to lack of memory.

Hibernation: Some Linux systems use swap space (especially a swap partition) to store the contents of RAM when the system is hibernated. The system saves the current memory state to swap, allowing it to restore the session when powered back on.

Checking and Managing Swap Space:
View Swap Usage:

free -h shows the total swap space and its usage.
swapon -s or cat /proc/swaps lists all active swap devices and swap files.
Changing Swap Size:

You can add swap space by creating a swap file or increasing the size of an existing swap partition.
To create a swap file:
bash
Copy
sudo dd if=/dev/zero of=/swapfile bs=1M count=2048
sudo mkswap /swapfile
sudo swapon /swapfile
Disable Swap: You can turn off swap with:

bash
Copy
sudo swapoff -a
Pros and Cons of Swap Space:
Pros:
Prevents Out-of-Memory (OOM) Errors: It can help prevent the system from crashing or killing processes when RAM is full.
Increased Capacity: Swap space allows the system to handle more processes than the physical RAM alone could accommodate.
Cons:
Slower Performance: Since disk storage is slower than RAM, relying heavily on swap space can degrade system performance.
Wear and Tear on SSDs: Constant swapping, especially on SSDs, can cause wear over time due to the limited number of write cycles on flash storage.
In summary, swap space helps ensure that Linux systems don't crash when they run out of physical RAM, but it is slower and should be used sparing.

### how to change the priority task

top

or

ps -eo pid,ni,comm | grep <process_name>

Set Priority When Starting a Process

Use nice to start a process with a specific priority:

nice -n <priority> <command>

Example:

nice -n 10 my_script.sh

Priority range: -20 (highest priority) to 19 (lowest priority)
Default priority is 0.

Change Priority of a Running Process

renice -n <priority> -p <PID>

Example:
renice -n -5 -p 1234
Requires root/sudo for increasing priority (-values).

To change priority as root:
sudo renice -n -10 -p 1234

Change CPU Scheduling Policy (Optional)
If you need more control over CPU scheduling, use chrt:
sudo chrt -r -p <priority> <PID>
sudo chrt -r -p 99 1234
FIFO (First In, First Out) and RR (Round Robin) policies require root access


SCP (Secure Copy Protocol)

Uses SSH for secure file transfer.
Only supports file transfer (no listing or managing remote files).

SFTP (SSH File Transfer Protocol)

Uses SSH for secure file transfer and remote file management.
Supports file listing, deletion, and directory navigation.

FTP (File Transfer Protocol)

An insecure protocol that transfers files over TCP (unencrypted).
Uses separate channels for commands (port 21) and data transfer.

Key Differences:

SCP & SFTP are secure (use SSH), while FTP is insecure.
SFTP supports file management, SCP does not.
FTP requires extra configurations for encryption (FTPS).

what is umask
umask (User File Creation Mask) controls the default permissions for new files and directories by subtracting values from the system defaults (666 for files, 777 for directories). For example, a umask of 022 results in 644 (rw-r--r--) for files and 755 (rwxr-xr-x) for directories.
when we create a new user user should notify that for every 30 days they should change the password
chage -M 30 -W 7 username
-M 30 → Sets password expiry to 30 days.
-W 7 → Warns the user 7 days before expiry.
