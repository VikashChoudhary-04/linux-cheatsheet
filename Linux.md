**# Linux Basic Commands Cheatsheet**



**## Navigation**

**-`pwd` : shows the current directory path**

**-`ls` : lists files and folders in a directory**

**-`ls -la`: List hidden files and show details** 

**-`ls -l`: List of files along with permission given to user, group and other users**

**-`ls -ld`: List of directories along with permission given to user, group and other users**

**-`ls -i filename`(Inode number): Show metadata like file type, permissions, owner, size, etc about the file**

**-`ls -i`: Show metadata like file type, permissions, owner, sized etc about all files in the directory**

**Inode is same for original file and hardlink file but different for softlink file**

**-`ls *`: Show all directories and all of their files (if any)**

**-`ls *d`: Show all directories and all of their files (if any) that starts with "d". This can be done for any letter.**

**-`ls *d*`: Show all directories and all of their files (if any) that has the letter "r" in them. This can be done for any letter.**

**-`ls [ca]*`: Show all directories that have 'c' and 'a' in their names.**

**-`command > FileName`: Store command's output in a file while replacing the data that was stored earlier (if any).**

**-`command >> FileName`: Store command's output in a file while appending it to the data thaty was stored earlier (if any).**

**- `cd foldername` : change to that folder ('cd' can be used to exit a folder)**

**- `cd ..` : go back one folder ('..' can be used for ls too)**



**## File Operations**

**- `touch file.txt` : create a new file**

**- `touch file1.txt file2.txt file3.txt`: Create multiple new (empty) files** 

**- `mkdir foldername` : create a new folder**

**- `mkdir /"directory path"/foldername -p` : create a folder within nested folders**

**- `mkdir /"directory path"/foldername -pv`: Show Step-by-step process of creation of folder**

**- `mkdir dir{1..10}` or `mkdir dir{a..e}`: Create multiple directories named as dir1, dir2,..., dir10 or as dira, dirb,...,dire. We can use any number or letter.**

**- `mkdir dir{1,3,5}`: Create specific multiple file (dir1, dir3, and dir5 in this case). We can use any number.**

**- `rm file.txt` : delete a file**

**- `rm -r foldername` : delete a folder and its contents**

**-`rm file.txt`: Delete a file**

**- `rm -r /Directory path/file.txt`: Delete a file from a directory** 

**- `rm -rf /Directory path/file.txt`: Delete file from a directory permanently without warning (Can be used to delete folders too)**

**- `rm -f file.txt`: Delete file permanently without warning** 

**- `cp file1.txt backup.txt`: Copy a file into another file**

**- `cp -r Dir1 Dir2`: Copy a folder/directory into another folder**

**- `mv oldname.txt newname.txt`: Rename a file**

**- `mv file.txt /Directory path`: Move a file into a folder/directory** 

**- `file filename.txt`: Checks the type of data in file (text, binary, image, etc)**

**- `tree directoryname`: Show content of directory/folder in tree like structure** 



**## Viewing Files**

**- `cat file.txt` : shows content of the file**

**- `cat file1.txt file2.txt > Merged.txt`: Merge content of two files into one**

**- `less file.txt` : Scrollable and ideal for reading view of a file**

**-`wc file.txt`: Count lines, words and characters in a file**

**-`wc -la file.txt`: Count lines (-w for words and -c for characters)**

**- `head file.txt` : shows first 10 lines**

**-`head -n 20 file.txt`: Shows first 20 lines (can choose any number in place of 20)**

**- `tail file.txt` : shows last 10 lines**

**-`tail -n 20 file.txt`: Shows last 20 lines (can choose any number in place of 20)**





**## System Info and other commands**

**- `whoami` : shows your username**

**- `date` : shows current date and time**

**- `date +%R`: Show time hours and minutes in 24 hours format**

**-`date +%T`: Show time hours, minutes and seconds in 24 hours format**

**-`date +%x`: Country specific date representation (similar commands for showing day, month, year, hour, minute, second, etc)**

**-`echo $(date +%A)`: Shows present day (like saturday).**

**- `clear` : clears the terminal**

**-`passwd---stdin Username`: Used to change a user's password** 

**-`Ps -u`: View running processes on the system** 

**-`exit`: Exit from current user**

**-`history`: Show all the commands used in the past**

**-`sudo -i`: Enter root user (After entering password)**

**-`##Text`: Write comment. Not considered part of the code while executing.** 

**-`ln original.txt hardlink.txt` : Create hardcopy file with exact data as original file (both files points to same content)**

**-`ln -s original.txt softlink.txt`: Create soft copy file with which points to same path but not content**

**-`variablename = value`: Storing a value in a variable (for example, intergers, strings, etc.**

**-`echo $variablename`: Accessing the variable (value of the variable).**

**-`env`: Gives list of all variables stored in the user's system.**

**-`man ls` or `ls --help`: Help and all information related to 'ls' command. It can be used for any command.**

**-`command1 ; command2`: Run two commands together at the same time.**

**-`find /etc -name passwd 2> FileName`: Writing all the errors coming from this command to a file and only displaying error-free code on screen. '2> /dev/null' to send errors to dustbin (won't be able to access). '2>&FileName' to write both errors and output in a file.**

**-`grep ParticularLetterOrLetters /DirectoryPath/FileName`: Find all occurance of that letter or letters(together) in a file.**

**-`echo 'Text' | Tee FileName`: Write the text in the file and also show it on screen.**

**-`vim Filename`: Edit and write in a file.**

**`Shift + i`: Enter Insert mode (for writing).**

**`:wq` or `Shift + zz`: Save changes and quit file in vim.**

**`3yy`: In Vim, Keep cursor at start of the text you want to copy. (In command mode) Type this to copy next 3 lines. You can choose any number of lines.**

**`p`: In vim, Press this in command mode to paste copied lines.**

**`o`: In vim command mode, keep you cursor on a particular line. Pressing this will add a line in between this line and the next line and we will enter insert mode.**

**`u`: In vim command mode, use this to undo a task when using Vim.**

**`q!`: Exit vim file without saving.**

**`10gg`: 10th line. It can be any number.**

**`:set number`: Show line numbers in vim file.**

**`/word`: To find occurance of the word in the file.**

**-`UserAdd Username` or `AddUser Username`: Add new user. Also creates a group with the same name.**

**-`id Username`: Information about username.**

**-`UserDel Username`: Delete user. This command is used by root user.**

**-`UserDel -r Username`: Delete user from /home directory.**

**-`cd ~`: Root's home directory.**

**-`cat /etc/passwd | grep UserName`: Show information about user.**

**-`usermod -c "Text" Username`: Add comment about user in user information.**

**-`usermod -l NewName OldName`: Change name of the user in user information. Changes shown only in configurations and not home directory.**

**-`!98`: Run 98th command from history again. It can be any number.**

**-`Usermod -s /sbin/nologin username`: Change shell of user information to not login.**

**-`Usermod -s /bin/bash UserName`: Change shell of user information to login.**

**-`Usermod -d /DirectoryPath -m Username`: Change user's home directory and shift its data too.**

**-`Usermod -u UserId Username`: Change user id of the user.**

**-`sudo UserAdd Username`: Allows creating new user even when not in root. It provides extra permissions.** 

**-`vim /etc/sudoers`: Used to give rights to other users by writing the username in the line next to the line for root. We can decide specific permissions for the user by changing "All".**


**-`GroupAdd GroupName`: Create group.**

**-`GroupDel GroupName`: Delete group.**

**-`Usermod -G Group name UserName`: Add a user to a group.**

**-`%GroupName ALL=(ALL) NOPASSWD:ALL`: Allows Sudo rights to a group without needing password. To be written in /etc/sudoers.**

**-`Usermod -aG GroupName UserName`: Add a user to another group without removing it from the original group.**

**-`PASS_MAX_DAYS`: Set number of days to change users' password after.**

**-`Useradd -G GroupName UserName`: Add user to a group during the time of its creation.**

**-`Useradd -u UserId UserName`: Add user along with its user ID. -c and others can also be added.**

**-`Groupmod -g 20000 GroupName`: Make changes to a group. Here we changed the group's Id.**

**-`Groupmod -n OldName NewName`: Change name of a group.**

**-`gpasswd -d UserName GroupName`: Remove a user from a group.**

**-`drwxr-xr-x 2 UserName GroupName 6 July 25 1:29 Directory/FileName`: d means its a directory (- for file). rwx is the read, write and execution permissions given to the owner. r-x is the read and execute permissions given to the group of the owner. r-x is the read and execute permissions given to other users.**

**-`chmod o+rwx /FilePath`: Gives reading, writing and execution permissions to o (other users). a can be used for all, u for owner (user) and g for group.**

**-`chmod r=a`: Give read permission to all. It can be done for w and x too.**

**-`Numeric method of permissions`**

**`0` = No permission**

**`1` = Execute**

**`2` = Write**

**`3` = Write and execute**

**`4` = Read**

**`5` = Read and execute** 

**`6` = Read and write**

**`7` = Read, Write and execute**

**Full permission = 777.**

**1st digit for owner user.**

**2nd digit for group.**

**3rd digit for other users.**

**-`chmod 700 /DirectoryPath`: This gives all 3 permissions to user and no permission to group and others.**

**-`chgrp GroupName DirectoryName`: Change group of a directory.**

**-`chown UserName DirectoryName`: Change the owner of a directory.**

**-`ip`: It gives information about internet protocol (IP) of virtual machine.**

**-`ping www.website.com`: Ping a popular website to check internet connection.**

**-`nmcli connection add type ethernet con-name my-connection`: Create a new connection. It is possible to run this command when the device is connected to internet.**

**-`nmcli connection modify my-connection ipv4.addresses 192.168.1.1/24 ipv4.dns 192.168.1.0 ipv4.gateway 192.168.1.2 method manual connection.autoconnect yes`: Make specified changes to the connection like ip address, DNS, gateway, method, etc. We can make changes to any one of these.**

**-`nmcli connection up my-connection`: Activate connection. In place of up, we can use down to deactivate the connection.**

**-`nmcli connection show my-connection`: Shows information about a connection like its ip address, DNS, etc.**

**-`nmcli connection delete my-connection`: Deletes a connection.**

**-`nmtui`: Execute commands in GUI mode.**

**-`[root@localhost ~]`: This is shown on the left side of each command in linux. 'root' is the username here. '@' is a seperator used to seperate 'root' and 'localhost'. 'localhost' is the machine's name. '~' represents the root's home directory.**

**-`alias`: Creates a shortcut (custom name) for a command or a sequence of commands to simplify repetitive command-line tasks.**

**-`alias ll='ls -la'`: Creates a temporary alias ll that executes the ls -la command in the current terminal session.**

**-`alias update='sudo apt update && sudo apt upgrade'`: Creates a temporary alias update to run system update and upgrade commands together.**

**-`nano ~/.bashrc`: Opens the Bash configuration file to add or modify permanent aliases.**

**-`source ~/.bashrc`: Reloads the Bash configuration file so newly added aliases take effect without restarting the terminal.**

**-`unalias ll`: Removes the alias ll from the current terminal session.**

**-`~/.bashrc`: A shell configuration file that runs at terminal startup and stores permanent aliases and shell settings.**
**-`hostnamectl set-hostname DesiredName`: It is used to change hostname to a desired name.**

**-`exit`: Terminates the current shell session and closes the terminal or returns to the previous shell.**

**-`logout`: Ends a login shell session; mainly used when working in a login shell environment.**

**-`env`: Displays all environment variables currently set for the active shell session.**

**-`echo $HOME`: Prints the path of the current user’s home directory stored in the HOME environment variable.**

**-`PATH`: An environment variable that defines the search locations for executable files when a command is run.**

**-`export TEST=test`: Creates an environment variable named TEST for the current terminal session.**

**-`~/.bashrc`: Bash configuration file used to store persistent environment variables for interactive shells.**

**-`~/.zshrc`: Zsh configuration file used to define persistent environment variables in Zsh shells.**

**-`~/.config/fish/config.fish`: Fish shell configuration file used to set persistent environment variables in Fish shell.**

**-`expand`: Converts tab characters in a file into spaces (8 spaces per tab by default) and outputs the result to standard output.**

**-`expand sample.txt`: Reads sample.txt and replaces all tab characters with spaces for consistent text formatting.**

**-`unexpand`: Converts spaces back into tab characters to reduce file size or follow tab-based formatting standards.**

**-`unexpand -a result.txt`: Converts all groups of spaces (not just leading spaces) in result.txt into tabs.**

**-`join`: Merges lines from two sorted files based on a common field (first field by default).**

**-`join file1.txt file2.txt`: Joins two files using their common first column as the matching key.**

**-`join -1 2 -2 1 file1.txt file2.txt`: Joins files by specifying field 2 from the first file and field 1 from the second file as the matching fields.**

**-`split`: Divides a large file into smaller files for easier management.**

**-`split somefile`: Splits somefile into multiple files of 1000 lines each by default (named xaa, xab, etc.).**

**-`tr`: Translates, deletes, or modifies characters from standard input; commonly used with pipes for text processing.**

**-`tr a-z A-Z`: Translates all lowercase letters to uppercase.**

**-`tr -d '0-9'`: Deletes all digits from the input stream.**

**-`tr -s ' '`: Squeezes repeated spaces into a single space to normalize text formatting.**

**-`uniq`: Removes duplicate adjacent lines from a file or standard input.**

**-`uniq reading.txt`: Outputs the file content with repeated adjacent lines removed.**

**-`uniq -c reading.txt`: Displays each line prefixed with the number of times it occurs consecutively.**

**-`uniq -u reading.txt`: Displays only lines that are not repeated (unique lines).**

**-`uniq -d reading.txt`: Displays only lines that are repeated.**

**-`sort`: Sorts lines of text alphabetically or numerically.**

**-`sort reading.txt | uniq`: Sorts the file first so identical lines become adjacent, then removes duplicates correctly.**

**-`nl`: Adds line numbers to each line of a file or standard input, making text easier to read and reference.**

**-`nl file1.txt`: Displays the contents of file1.txt with line numbers prefixed to each line.**

**-`emacs`: Launches the Emacs text editor, a highly powerful and extensible editor used for editing files, writing code, and performing many system tasks within a single environment.**

- C-x C-s: Saves the currently open file in Emacs.

- C-x C-w: Saves the current buffer with a new filename (“Save As”).

- C-x s: Saves all modified buffers, prompting for confirmation if needed.

- C-x C-f: Opens an existing file or creates a new file in Emacs; can also open directories.

- C-x b: Switches to another buffer by prompting for the buffer name.

- C-x → (right arrow): Cycles to the next open buffer.

- C-x ← (left arrow): Cycles to the previous open buffer.

- C-x 2: Splits the current window vertically into two windows.

- C-x o: Moves the cursor to the other window in a split view.

- C-x 1: Closes all other windows, keeping only the current window visible.

- C-x k: Kills (closes) the current buffer.

- C-↑ (Ctrl + Up Arrow): Moves the cursor up by one paragraph.

- C-↓ (Ctrl + Down Arrow): Moves the cursor down by one paragraph.

- C-← (Ctrl + Left Arrow): Moves the cursor one word to the left.

- C-→ (Ctrl + Right Arrow): Moves the cursor one word to the right.

- M->: Moves the cursor to the end of the buffer.

- C-space: Sets the mark to begin selecting a region of text.

- C-w: Kills (cuts) the selected region of text.

- C-y: Yanks (pastes) the most recently killed text.

- C-x C-c: Exits Emacs; prompts to save any unsaved buffers before closing.

- C-h C-h: Opens the Emacs help menu for guidance and documentation.

- C-x u: Undoes the last action in Emacs.

- su: Switches the current user to another user (root by default) by starting a new shell after password authentication.

- visudo: Safely edits the /etc/sudoers file with syntax checking to prevent configuration errors that could break sudo access.

- vipw: Safely edits the /etc/passwd file by locking it during editing to prevent corruption and syntax errors.

- adduser: An interactive, user-friendly command for creating a new user account, which prompts for details like password and user information while setting up the account automatically.

- umask: Sets the default permission mask that determines which permissions are removed from newly created files and directories.

- umask 021: Configures default permissions so the user has full access, the group loses write permission, and others lose execute permission for newly created files.

- ps aux: Displays all processes for all users in a detailed, user-oriented format, including processes without a controlling terminal.

- ps -ef: Shows a full-format listing of all processes on the system, including parent-child relationships and start times.

- ps -e: Lists all running processes on the system (less detailed than ps -ef).

- top: Provides a real-time, continuously updating view of running processes and system resource usage (CPU, memory, etc.).

- ps l: Displays running processes in long-format output, including the PPID (Parent Process ID), which helps observe parent–child process relationships.

- kill: Sends a signal to a process (by PID) to control its behavior, most commonly to request termination (SIGTERM by default or SIGKILL for forceful termination).

- kill <PID>: Sends the default SIGTERM (signal 15) to a process, requesting graceful termination.

- kill -15 <PID>: Explicitly sends SIGTERM (polite termination request) to a process.

- kill -9 <PID>: Sends SIGKILL (signal 9) to immediately and forcefully terminate a process without cleanup.

- kill -1 <PID>: Sends SIGHUP (signal 1), commonly used to tell daemon processes to reload configuration files.

- kill -2 <PID>: Sends SIGINT (signal 2), equivalent to pressing Ctrl-C in the terminal.

- kill -19 <PID>: Sends SIGSTOP (signal 19) to pause a process without terminating it.

- kill -0 <PID>: Checks whether a process exists and whether the user has permission to signal it (does not terminate the process).

- nice: Starts a new process with a specified niceness (priority) value to influence CPU scheduling.

- nice -n 5 <command>: Launches a command with a niceness value of 5, giving it lower priority than default processes.

- renice: Changes the niceness (priority) of an already running process.

- renice 10 -p <PID>: Sets the niceness value of the running process with the given PID to 10, lowering its CPU priority.

- htop: An interactive, enhanced process viewer that reads data from /proc to display real-time system and process information in a user-friendly interface.

- sleep: Pauses execution for a specified amount of time (in seconds), commonly used to demonstrate job control and background execution.

- sleep 1000 &: Runs the sleep command in the background, immediately returning the shell prompt.

- jobs: Lists all jobs running in the background or suspended within the current shell session.

- bg: Resumes a suspended job and runs it in the background.

- fg: Brings a background or suspended job to the foreground.

- fg %<job_id>: Brings a specific background job (identified by job ID) to the foreground.

- kill %<job_id>: Sends a signal to a job using its job ID instead of a process ID (PID).

- gzip: Compresses a single file, replacing it with a .gz compressed version.

- gzip <filename>: Compresses the specified file and creates <filename>.gz.

- gunzip: Decompresses a .gz file and restores the original file.

- gunzip <filename>.gz: Decompresses a gzip-compressed file.

- tar: Creates, extracts, and manages archive files (tarballs).

- tar cvf <archive>.tar <files>: Creates a new tar archive containing specified files or directories.

- tar czvf <archive>.tar.gz <files>: Creates a gzip-compressed tar archive in a single step.

- tar xvf <archive>.tar: Extracts files from a tar archive.

- tar xzvf <archive>.tar.gz: Decompresses and extracts a gzip-compressed tar archive.

- dpkg: Low-level package management command for installing, removing, and querying .deb packages on Debian-based systems.

- dpkg -i <package>.deb: Installs a Debian package file (.deb) without resolving dependencies.

- dpkg -r <package>: Removes an installed Debian package but keeps configuration files.

- dpkg -l: Lists all installed Debian packages on the system.

- rpm: Low-level package management command for installing, removing, and querying .rpm packages on Red Hat–based systems.

- rpm -i <package>.rpm: Installs an RPM package file without resolving dependencies.

- rpm -e <package>: Removes (erases) an installed RPM package.

- rpm -qa: Lists all installed RPM packages (q = query, a = all).

- apt: High-level package manager for Debian-based systems used to install, update, remove, and inspect software packages.

- apt install <package>: Installs a package from configured repositories and automatically resolves dependencies.

- apt remove <package>: Removes an installed package while keeping configuration files.

- apt update: Refreshes the local package index with the latest information from repositories.

- apt upgrade: Upgrades all installed packages to their latest available versions.

- apt show <package>: Displays detailed information about a package (version, size, description, dependencies).

- yum: Package manager for RPM-based systems (RHEL, CentOS, Fedora) that installs, updates, and removes software with dependency handling.

- yum install <package>: Installs a package and all required dependencies from repositories.

- yum erase <package>: Removes an installed package from the system.

- yum update: Updates all installed packages and refreshes package metadata.

- yum info <package>: Shows detailed information about a specific package.

- ./configure: Runs the configuration script to check system dependencies and prepare the source code for compilation.

- make: Compiles the source code according to rules defined in the Makefile.

- make install: Installs the compiled software into system directories (usually requires superuser privileges).

- checkinstall: Creates and installs a native system package (e.g., .deb) from compiled source code, allowing clean package management.

- make uninstall: Attempts to remove software installed from source by reversing the installation steps (only works if supported by the Makefile).

- mknod: Manually creates a device node (special file) in /dev by specifying its type and major/minor numbers.

- mknod /dev/sdb1 b 8 3: Creates a block device named /dev/sdb1 with major number 8 and minor number 3.

- udevadm: Queries and controls the udev device manager, allowing inspection of device metadata and rules.

- udevadm info --query=all --name=/dev/sda: Displays detailed udev and sysfs information for the specified device.

- lsusb: Lists all USB devices connected to the system along with basic identification details.

- lsusb -t: Displays USB devices in a hierarchical (tree-like) structure showing hubs and device relationships.

- lspci: Lists all PCI devices such as graphics cards, network adapters, and sound cards.

- lssci: Lists SCSI and SATA storage devices, including hard drives, SSDs, and optical drives.

- dd: Copies and converts data at a low level by reading from an input source and writing to an output destination, commonly used for disk imaging and backups.

- dd if=<input> of=<output>: Copies data from the specified input file or device to the specified output file or device.

- dd if=<input> of=<output> bs=<bytes>: Copies data using a specified block size to control read/write performance.

- dd if=<input> of=<output> bs=<bytes> count=<number>: Copies a fixed amount of data defined by block size multiplied by count.

- ls -l /: Lists all top-level directories in the root (/) filesystem with detailed information such as permissions, ownership, size, and timestamps.

- df -T: Displays disk space usage for all mounted filesystems and shows their filesystem types (e.g., ext4, xfs, tmpfs).

- sudo parted -l: Lists all disks and their partition tables (MBR/GPT), showing partition layout, sizes, filesystem types, and flags.

- fdisk: A command-line disk partitioning tool used for managing MBR partition tables (does not support GPT).

- gparted: A graphical disk partitioning tool (GUI) that supports both MBR and GPT and provides a visual alternative to command-line tools.

- gdisk: A command-line disk partitioning tool similar to fdisk, but designed specifically for GPT partition tables.

- sudo parted: Launches the parted utility in interactive mode for manually managing disk partitions.

- select /dev/sdb: (inside parted) Selects the target disk device to operate on.

- print: (inside parted) Displays the current partition table of the selected disk.

- mkpart primary ext4 1MB 5000MB: (inside parted) Creates a primary partition formatted as ext4 between the specified start and end points.

- resizepart 1 8000MB: (inside parted) Resizes partition number 1 to a new end position at 8000MB.

- resize2fs: Resizes an ext2/ext3/ext4 filesystem to match the size of its underlying partition.

- mkfs: Creates (formats) a filesystem on a disk partition so it can store files and directories.

- mkfs -t ext4 /dev/sdb2: Creates an ext4 filesystem on the partition /dev/sdb2.

- mount: Attaches a filesystem from a device to a directory (mount point) so it can be accessed.

- mount -t ext4 /dev/sdb2 /mydrive: Mounts an ext4 filesystem from /dev/sdb2 to the directory /mydrive.

- umount: Detaches a mounted filesystem safely from the system.

- umount /mydrive: Unmounts a filesystem using its mount point.

- umount /dev/sdb2: Unmounts a filesystem using the device name.

- blkid: Displays block device attributes such as UUID and filesystem type.

- mount UUID=<uuid> /mydrive: Mounts a filesystem using its UUID instead of a device name for stable identification.

- cat /etc/fstab: Displays the contents of the /etc/fstab file to review configured filesystems that are mounted at boot.

- mount -a: Mounts all filesystems defined in /etc/fstab (except those marked with the noauto option), useful for testing fstab entries without rebooting.

- mkswap /dev/sdb2: Initializes a partition or file to be used as Linux swap space.

- swapon /dev/sdb2: Enables the specified swap partition or file, making it available as virtual memory.

- swapoff /dev/sdb2: Disables the specified swap partition or file, removing it from active swap usage.

- df: Shows disk space usage of mounted filesystems (total, used, available).

- du: Shows disk usage of files and directories to identify space consumption.

- fsck: Checks and repairs filesystem inconsistencies caused by crashes, power failures, or corruption.

- stat: Displays detailed inode and file metadata such as permissions, ownership, timestamps, size, inode number, and block allocation.

- strace: Traces and displays system calls and signals made by a program, helping you understand how a process interacts with the Linux kernel (commonly used for debugging).

- uname: Displays system information; commonly used to check the currently running kernel version (e.g., with uname -r).

- lsmod: Displays a list of all kernel modules currently loaded into the Linux kernel.

- modprobe: Loads or unloads kernel modules and automatically handles module dependencies.

- service: Manages system services on System V–based (and compatible) init systems.

- service --status-all: Lists all available services and shows whether each service is running, stopped, or in an unknown state.

- service start: Starts a specified service.

- service stop: Stops a specified running service.

- service restart: Stops and then starts a service again, commonly used after configuration changes.

- initctl: Primary command-line utility to manage Upstart jobs and events.

- initctl list: Lists all Upstart jobs along with their current goal and status.

- initctl status: Shows the current status of a specific Upstart job.

- initctl start: Manually starts a specified Upstart job.

- initctl stop: Manually stops a running Upstart job.

- initctl restart: Restarts a job by stopping and then starting it again.

- initctl emit: Emits a custom event that can trigger one or more Upstart jobs configured to listen for that event.

- systemctl list-units: Lists all active systemd units currently managed by the system.

- systemctl status networking.service: Displays the current status, activity state, and recent logs of the networking service.

- sudo systemctl start networking.service: Starts the networking service immediately.

- sudo systemctl stop networking.service: Stops the networking service if it is running.

- sudo systemctl restart networking.service: Stops and then starts the networking service again.

- sudo systemctl enable networking.service: Configures the networking service to start automatically at system boot.

- sudo systemctl disable networking.service: Prevents the networking service from starting automatically at boot.

- top: Displays a real-time, dynamic view of running processes and overall system resource utilization (CPU, memory, tasks)

- uptime: Shows how long the system has been running, number of logged-in users, and load averages (same info as the first line of top)

- top -p 1: Displays real-time resource usage for a specific process by PID (here, PID 1)

- lsof: Lists all open files on the system along with the processes that opened them (files, directories, sockets, devices)

- lsof .: Shows which processes are currently using the present working directory

- fuser: Identifies processes (PIDs) that are accessing a specific file, directory, or filesystem

- fuser -v .: Displays verbose information about which processes are using the current directory and how they are accessing it

- fuser -k /mnt/usb: Sends a SIGKILL signal to all processes using the /mnt/usb mount point, freeing the resource so it can be unmounted

- ps m: Displays processes along with their threads, showing threads listed under their parent process

- uptime: Displays the current time, system uptime, number of logged-in users, and the system load average over the last 1, 5, and 15 minutes

- cat /proc/cpuinfo: Shows detailed information about the CPU, including the number of cores, which helps interpret load average correctly

- iostat: Displays CPU utilization statistics and detailed disk I/O activity, including read/write rates, transfers per second, and I/O wait indicators

- vmstat: Reports system performance statistics, including processes, memory usage, swap activity, I/O, interrupts, context switches, and CPU utilization

- apt install sysstat: Installs the sysstat package, which provides the sar tool for historical system monitoring

- sar -q: Displays system load and run-queue statistics collected from the start of the current day

- sar -r: Displays memory usage statistics collected from the start of the current day

- sar -P: Displays CPU usage statistics

- sar -q /var/log/sysstat/saXX: Displays load statistics for a specific day using the corresponding sysstat log file (where XX is the day number, e.g., sa02)

- crontab -e: Opens the current user’s crontab file in an editor to add or modify scheduled jobs

- crontab -l: Lists all cron jobs scheduled for the current user

- crontab -r: Removes all cron jobs for the current user

- 30 08 * * * /home/pete/scripts/change_wallpaper: Cron job entry that runs the script every day at 8:30 AM

- /home/pete/scripts/change_wallpaper: Script executed by cron according to the defined schedule
