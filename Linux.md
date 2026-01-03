# 🐧 Linux Commands Cheatsheet (LOSSLESS & ARRANGED)

---

## 1️⃣ Navigation, Prompt & Directory Awareness

* `pwd` : shows the current directory path
* `ls` : lists files and folders in a directory
* `ls -la` : List hidden files and show details
* `ls -l` : List of files along with permission given to user, group and other users
* `ls -ld` : List of directories along with permission given to user, group and other users
* `ls -i filename` : Show inode number of the file
* `ls -i` : Show inode numbers of all files in directory
* `ls *` : Show all directories and all of their files (if any)
* `ls *d` : Show all directories/files starting with "d"
* `ls *d*` : Show all directories/files containing letter "d"
* `ls [ca]*` : Show all directories/files starting with c or a
* `cd foldername` : change to that folder
* `cd ..` : go back one folder
* `cd ~` : Root's home directory
* `[root@localhost ~]` : Linux prompt explanation

---

## 2️⃣ File Creation & Directory Creation

* `touch file.txt` : create a new file
* `touch file1.txt file2.txt file3.txt` : Create multiple files
* `mkdir foldername` : create a new folder
* `mkdir /directory/path/foldername -p` : create nested directories
* `mkdir /directory/path/foldername -pv` : verbose directory creation
* `mkdir dir{1..10}` : Create multiple numbered directories
* `mkdir dir{a..e}` : Create multiple alphabet directories
* `mkdir dir{1,3,5}` : Create specific directories

---

## 3️⃣ File & Directory Deletion

* `rm file.txt` : delete a file
* `rm -r foldername` : delete folder and contents
* `rm -r /Directory path/file.txt` : Delete file from directory
* `rm -rf /Directory path/file.txt` : Permanent delete without warning
* `rm -f file.txt` : Force delete file

---

## 4️⃣ Copy, Move & Rename

* `cp file1.txt backup.txt` : Copy a file
* `cp -r Dir1 Dir2` : Copy directory
* `mv oldname.txt newname.txt` : Rename file
* `mv file.txt /Directory path` : Move file

---

## 5️⃣ File Identification & Structure

* `file filename.txt` : Identify file type
* `tree directoryname` : Tree structure
* `stat` : Display inode and file metadata

---

## 6️⃣ Viewing & Reading Files

* `cat file.txt` : Show file contents
* `cat file1.txt file2.txt > Merged.txt` : Merge files
* `less file.txt` : Scrollable viewer
* `wc file.txt` : Count lines, words, characters
* `wc -la file.txt` : Line count
* `head file.txt` : First 10 lines
* `head -n 20 file.txt` : First 20 lines
* `tail file.txt` : Last 10 lines
* `tail -n 20 file.txt` : Last 20 lines

---

## 7️⃣ Redirection, Pipes & Text Processing

* `command > FileName` : Redirect output (overwrite)
* `command >> FileName` : Redirect output (append)
* `find /etc -name passwd 2> FileName` : Redirect errors
* `2> /dev/null` : Discard errors
* `2>&FileName` : Redirect output + errors
* `grep letters file` : Search text
* `echo 'Text' | tee FileName` : Output + save
* `expand sample.txt` : Tabs to spaces
* `unexpand -a result.txt` : Spaces to tabs
* `join file1.txt file2.txt` : Join files
* `join -1 2 -2 1 file1 file2` : Custom join
* `split somefile` : Split file
* `tr a-z A-Z` : Lower to upper
* `tr -d '0-9'` : Delete digits
* `tr -s ' '` : Remove extra spaces
* `uniq reading.txt` : Remove duplicates
* `uniq -c reading.txt` : Count duplicates
* `uniq -u reading.txt` : Unique only
* `uniq -d reading.txt` : Duplicates only
* `sort reading.txt | uniq` : Correct duplicate removal
* `nl file1.txt` : Line numbering

---

## 8️⃣ Editors (Vim)

* `vim Filename` : Edit file
* `Shift + i` : Insert mode
* `:wq` : Save and quit
* `Shift + zz` : Save and quit
* `3yy` : Copy 3 lines
* `p` : Paste
* `o` : Insert new line
* `u` : Undo
* `q!` : Quit without saving
* `10gg` : Go to line 10
* `:set number` : Line numbers
* `/word` : Search word

---

## 9️⃣ Editors (Emacs)

* `emacs` : Launch editor
* `C-x C-s` : Save file
* `C-x C-w` : Save as
* `C-x s` : Save all buffers
* `C-x C-f` : Open file
* `C-x b` : Switch buffer
* `C-x → / ←` : Cycle buffers
* `C-x 2` : Split window
* `C-x o` : Switch window
* `C-x 1` : Close other windows
* `C-x k` : Kill buffer
* `C-space` : Set mark
* `C-w` : Cut
* `C-y` : Paste
* `C-x C-c` : Exit Emacs
* `C-h C-h` : Help
* `C-x u` : Undo

---

## 🔟 Environment Variables & Shell

* `variablename=value` : Store variable
* `echo $variablename` : Access variable
* `env` : List variables
* `export TEST=test` : Export variable
* `PATH` : Executable search path
* `alias` : Create alias
* `alias ll='ls -la'` : Alias example
* `unalias ll` : Remove alias
* `nano ~/.bashrc` : Edit bash config
* `source ~/.bashrc` : Reload bash config
* `exit` : Exit shell
* `logout` : Logout shell

---

## 1️⃣1️⃣ User & Group Management

### Users

* `useradd Username` : Create user
* `adduser Username` : Interactive user creation
* `userdel Username` : Delete user
* `userdel -r Username` : Delete user + home
* `id Username` : User info
* `passwd --stdin Username` : Change password
* `usermod -c "Text" Username` : Comment
* `usermod -l New Old` : Rename user
* `usermod -s /sbin/nologin Username` : Disable login
* `usermod -s /bin/bash Username` : Enable login
* `usermod -d /path -m Username` : Change home
* `usermod -u UID Username` : Change UID
* `sudo useradd Username` : Create user with sudo

### Groups

* `groupadd GroupName` : Create group
* `groupdel GroupName` : Delete group
* `groupmod -g 20000 GroupName` : Change GID
* `groupmod -n Old New` : Rename group
* `usermod -G Group User` : Add user to group
* `usermod -aG Group User` : Append group
* `gpasswd -d User Group` : Remove user

---

## 1️⃣2️⃣ Permissions & Ownership

* `drwxr-xr-x` : Permission explanation
* `chmod o+rwx file` : Permission symbolic
* `chmod r=a` : Read to all
* `chmod 700 path` : Numeric permission
* `chown User file` : Change owner
* `chgrp Group file` : Change group
* `umask` : Default permission mask
* `umask 021` : Custom mask

---

## 1️⃣3️⃣ Processes, Jobs & Monitoring

* `ps aux` : All processes
* `ps -ef` : Full format
* `ps -e` : All running
* `ps l` : Long format
* `ps m` : Threads
* `top` : Live process monitor
* `top -p 1` : Monitor PID
* `htop` : Enhanced top
* `kill PID` : Kill process
* `kill -9 PID` : Force kill
* `nice -n 5 cmd` : Set priority
* `renice 10 -p PID` : Change priority
* `sleep 1000 &` : Background job
* `jobs` : List jobs
* `bg` : Resume background
* `fg %id` : Foreground job
* `uptime` : System uptime
* `lsof` : Open files
* `fuser -k /mnt` : Kill using mount

---

## 1️⃣4️⃣ Networking (FULL)

* `ifconfig -a` : Show interfaces
* `ip addr show` : Modern IP view
* `ip link show` : Interface info
* `ip link set eth0 up/down` : Enable/disable
* `ip address add` : Assign IP
* `route -n` : Routing table
* `ip route add` : Add route
* `ip route delete` : Delete route
* `dhclient` : DHCP request
* `ping host` : Connectivity
* `ping -c 3 host` : Limited ping
* `traceroute host` : Path trace
* `netstat -a/-t/-at` : Network sockets
* `nslookup domain` : DNS lookup
* `dig domain` : Detailed DNS
* `/etc/hosts` : Static host mapping

---

## 1️⃣5️⃣ Disk, Filesystem & Storage

* `df` : Disk usage
* `df -T` : Filesystem type
* `du` : Directory usage
* `ls -l /` : Root directories
* `blkid` : UUID info
* `fdisk` : MBR partition
* `gdisk` : GPT partition
* `parted` : Disk tool
* `mkfs -t ext4` : Format filesystem
* `mount device path` : Mount FS
* `umount device/path` : Unmount
* `cat /etc/fstab` : Auto mount config
* `mount -a` : Mount all
* `mkswap` : Create swap
* `swapon` : Enable swap
* `swapoff` : Disable swap
* `fsck` : Filesystem check
* `dd if= of=` : Disk copy

---

## 1️⃣6️⃣ Packages & Compilation

* `apt install/remove/update/upgrade` : Debian packages
* `dpkg -i/-r/-l` : Low-level deb
* `yum install/erase/update/info` : RPM manager
* `rpm -i/-e/-qa` : Low-level rpm
* `./configure` : Configure source
* `make` : Compile
* `make install` : Install
* `make uninstall` : Remove
* `checkinstall` : Package from source

---

## 1️⃣7️⃣ Services & Logging

* `service start/stop/restart` : SysV service
* `systemctl start/stop/restart` : systemd
* `systemctl enable/disable` : Boot service
* `dmesg` : Kernel logs
* `/var/log/syslog` : System logs
* `/var/log/messages` : System logs
* `/var/log/auth.log` : Auth logs
* `logger "text"` : Write log
* `logrotate` : Rotate logs

---

## 1️⃣8️⃣ File Transfer & Sharing

* `scp source dest` : Secure copy
* `rsync -avh` : Sync files
* `python -m http.server` : HTTP share
* `mount server:/dir` : NFS mount
* `smbclient //host/share` : Samba client

---

## 1️⃣9️⃣ Help & History

* `man command` : Manual
* `command --help` : Help
* `history` : Command history
* `!98` : Run command 98
