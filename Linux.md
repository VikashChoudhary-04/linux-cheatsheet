**# Linux Basic Commands Cheatsheet**



**## Navigation**

**- pwd : shows the current directory path**

**- ls : lists files and folders in a directory**

**- 'ls -la' = List hidden files and show details** 

**- cd foldername : change to that folder ('cd' can be used to exit a folder)**

**- cd .. : go back one folder ('..' can be used for ls too)**



**## File Operations**

**- touch file.txt : create a new file**

**- 'touch file1.txt file2.txt file3.txt': Create multiple new (empty) files** 

**- mkdir foldername : create a new folder**

**- 'mkdir /"directory path"/foldername -p' : create a folder within nested folders**

**- 'mkdir /"directory path"/foldername -p' (Step-by-step process)**

**- rm file.txt : delete a file**

**- rm -r foldername : delete a folder and its contents**

**-'rm file.txt': Delete a file**

**- 'rm -r /Directory path/file.txt': Delete a file from a directory** 

**- 'rm -rf /Directory path/file.txt': Delete file from a directory permanently without warning (Can be used to delete folders too)**

**- 'rm -f file.txt': Delete file permanently without warning** 

**- 'cp file1.txt backup.txt': Copy a file into another file**

**- 'cp -r Dir1 Dir2': Copy a folder/directory into another folder**

**- 'mv oldname.txt newname.txt': Rename a file**

**- 'mv file.txt /Directory path': Move a file into a folder/directory** 

**- 'file filename.txt': Checks the type of data in file (text, binary, image, etc)**

**- 'tree directoryname': Show content of directory/folder in tree like structure** 



**## Viewing Files**

**- cat file.txt : shows content of the file**

**- 'cat file1.txt file2.txt > Merged.txt': Merge content of two files into one**

**- less file.txt : Scrollable and ideal for reading view of a file**

**-'wc file.txt': Count lines, words and characters in a file**

**-'wc -la file.txt': Count lines (-w for words and -c for characters)**

**- head file.txt : shows first 10 lines**

**-'head -n 20 file.txt': Shows first 20 lines (can choose any number in place of 20)**

**- tail file.txt : shows last 10 lines**

**-'tail -n 20 file.txt': Shows last 20 lines (can choose any number in place of 20)**





**## System Info**

**- whoami : shows your username**

**- date : shows current date and time**

**-'date +%R': Show time hours and minutes in 24 hours format**

**-'date +%T': Show time hours, minutes and seconds in 24 hours format**

**-'date +%x': Country specific date representation (similar commands for showing day, month, year, hour, minute, second, etc)**

**- clear : clears the terminal**

**-'passwd---stdin Username': Used to change a user's password** 

**-'Ps -u': View running processes on the system** 

**-'exit': Exit from current user**

**-'history': Show all the commands used in the past**

**-'sudo -i': Enter root user (After entering password)**

**-'##Text': Write comment** 

**-'ln original.txt hardlink.txt' : Create hardcopy file with exact data as original file (both files points to same content)**

**-'ln -s original.txt softlink.txt': Create soft copy file with which points to same path but not content)**

