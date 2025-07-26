**# Linux Basic Commands Cheatsheet**



**## Navigation**

**- `pwd` : shows the current directory path**

**- `ls` : lists files and folders in a directory**

**- `ls -la` = List hidden files and show details** 

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

**-`vim Filename`: Edit and write in a file.
**`Shift + i`: Enter Insert mode (for writing).**
**`:wq`: Save changes and quit file.**
**`3yy`: Keep cursor at start of the text you want to copy. (In command mode) Type this to copy next 3 lines. You can choose any number of lines.**
**`p`: Press this in command mode to paste copied lines.**
**`o`: In command mode, keep you cursor on a particular line. Pressing this will add a line in between this line and the next line and we will enter insert mode.**
**`u`: In command mode, use this to undo a task when using Vim.**
