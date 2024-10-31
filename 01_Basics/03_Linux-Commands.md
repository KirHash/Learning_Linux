# Basic Linux Commands

## `pwd`

-user's current location (Present Work Directory)

## `whoami`

-displays the name of the current logged-in user

## `date`

-displays current time and date

### `date +%D`

-only displays the current date

### `date +%T`

-only displays the current time

### `date +%H:%M:%S`

-only displays the current time in hour(%H), minute(%M) and seconds(%S)

## `ls`

-displays directories or folders in the current location

### `ls -lt`

-displays files and directories in current location

### `ls -ltr`

-displays files and directories in current location but in reverse sorting to displays the recent modified files at the bottommost

### `ls -lh`

-displays files and directories in current location bwith human readabile size of the files

### `ls <matching-content>*`

-to find files with specific letters

### `ls *.<matching-extension>`

-to find files with specific extension

## `clear`

-clears the console

# Commands for Creating, Deleting and Editing files

## `cat <fileName>`

-to read the file's data

## `less <fileName>`

-to read the file and to search for a word '/' with the desired search name can be used and to Quit use 'Q'

## `touch <fileName>`

-to create a file

## `rm <fileName>`

-to delete a file

## `vi <fileName>`

-to create a file and edit the same file as well
<br>
-creates a new terminal, to insert or edit data use 'I', to end editing use 'esc' and to save the file use 'SHIFT + :wq'

## `nano <fileName>`

-It works just like 'vi' but it is more advanced and helpful to beginners

## `sort <fileName>`

-to sort the content of the file

## `sort -r <fileName>`

-to sort the content of the file in reverse

## `sort <fileName> | uniq`

-to display unique content in the file

## `split -l <Number of splits> <fileName>`

-to split a file in certain different files

## `grep "word" <fileName>`

-to search a word and display matching content from a file

## `egrep "word1|word2" <fileName>`

-to search multiple words and display matching content from a file

## `shuf <fileName>`

-to shuffle the content in a file

## `wc -l <fileName>`

-to count the number of lines in a file

# Working with Folders

## `mkdir <directoryName>`

-to create a folder

## `rmdir <directoryName>`

-to delete a folder

## `cd /path/folder`

-to change path or move to another folder

### `cd ..`

-to go back to the one previous folder or path

### `cd ../..`

-to go back to the two previous folder or path

## `cp <fileName> /dest/path`

-to copy and paste a file from one folder to another

## `cp <fileName_1> <fileName_2>`

-to copy content of File 1 to File 2

## `mv <fileName> /dest/path`

-to cut and paste a file from one folder to another

## `mv <fileName> <newFileName>`

-rename a file

## `head -<Number of lines to display> <fileName>`

-to display only certain number of top lines of a file

## `tail -<Number of lines to display> <fileName>`

-to display only certain number of bottom lines of a file

## `find /path/ -name <fileName>`

-to find a file (It is case sensitive)

## `locate <fileName>`

-to find a file
<br>
<br>
NOTE: It has a difference as compare to 'find' command that it has a database in which it stores all the files and directories to find its location. If a new file or folder has been created at the same then it won't be able to find its respective location since the database is not updated with the accordance of the creation of a new file
<br>
So, we have to have to use `updatedb` command to update its database. But it required root access

# Comparing files

## `cmp <fileA> <fileB>`

-to check if two files are identical or not

## `diff -u <fileA> <fileB>`

-to compare two files and display the differences

# Utility Commands

## `history`

-to display previously used commands

## `history | grep sort`

-to display specific previously used commands in a sorted manner

## `man <command>`

-provides a manual regarding a command

## `which <command>`

-to check which executable is the command using

## `bc`

-to use calculator

## `cal`

-to check calender of present

### `cal <month> <year>`

-to check calender of specific month and year

## `uptime`

-to display how long linux server is up and running for

## `script`

-used to record the activity on terminal and exit use '^D'

## `alias <abbreviated_alias>='<command>'`

-to create an alias for a command

# Compression and Decompression of files and folders

## `gzip -k <fileName>`

-to compress a file

## `gzip -d <fileName>` or `gunzip <fileName>`

-to decompress a file

## `tar -czf <zippedFolderName>.tar.gz <folderName>`

-to compress a folder

## `tar -xzf <zippedFolderName>.tar.gz`

-to decompress a folder

## `zip <zippedFileName>.zip file1 file2`

-to compress multiple files in a folder

## `unzip <zippedFileName>.zip`

-to decompress multiple files that are compress into one

## `unzip -l <zippedFileName>.zip`

-to list files in a zipped file

# Downloading

## `wget <URL_of_file>`

-to download a file from internet

## `wget -O <specifcName>.<extension> <URL_of_file>`

-to download a file from internet with specific saved name

## `curl <URL_of_API>`

-to call an API

## `apt`(Ubuntu) or `yum/dnf`(CentOS, Redhat, Fedora)

-to install an application that requires root privileges

## `rpm -qa | grep <packageName>`

-displays the installed packaged

## `dnf list installed`

-displays installed packages in the system

## `dnf list installed | grep <packageName>`

-displays specific installed packages in the system

## `apt search <packageName>`(Ubuntu) or `yum/dnf list available | grep <packageName>`(CentOS, Redhat, Fedora)

-to list available packages to install

# Linux Service Control

## `systemctl start/stop <serviceName>.service`

-to start or stop a service

## `systemctl status <serviceName>.service`

-to check the status of a service

## `systemctl list-units --type=service --all`

-to list all services

# Environment Variables check

## `printenv`

-to check the environment variables in the system

## `export <envName>="Path"` and `export PATH=$<envName>/bin:$PATH`

-to add and setup a new environment variable path temporarily

## `source .bashrc` or `source ~/.bash_profile`

-to add and setup a new environment variable path permanently

NOTE: Add the env var in the ./bashrc file after exporting the variable by `export VARIABLE` or directly by `export VARIABLE=VALUE`

# String Operations Commands

## `awk -F <seperator> '{print $<column>}' <file>`

-to print specific column from a csv file

## `cut -c<startRange-endRange> <file>`

-to display starting two characters of all lines

## `sed -n '<numberOfLine>p' <file>`

-to display a specific line from a file

## `sed 's/<from>/<to>/g' <file>`

-to display a specific word from a file

## `tr [:lower:] [:upper:] <file` or `tr [:upper:] [:lower:] <file`

-to convert the content to Uppercase or Lowercase within a file

### `tr -d 'Char_to_be_deleted' <file`

-to delete a character within the file

### `tr "from_character" "to_character" <file`

-to replace the character with the chosen character within the file

## `truncate -s <desired_size> <file>`

-to change the size of the file

# Access Remote Linux Server

## `ssh user@hostname`

-to access remote linux server

## `scp file user@hostname:/location/`

-to copy a file to a remote linux server

# Working with Permissions

## `ls -ltr`

-to check permissions of a file

1. rwx : Read, Write, Executable Permissions
2. rw- : Read, Write Permissions
3. r-- : Read Permissions

## `chmod u/g/o/a+rwx/rw/r <file>`

-to modify permissions of a file

1. u: user
2. g: group
3. o: other
4. a: all

## `chown <newOwner> <file>`

-to change the ownership of a file

## `chgrp <newGrpOwner> <file>`

-to change the group ownership of a file

# Memory Information commands

## `free`

-to check free RAM space

### `free -h`

-to check free RAM space with human readability

### `free -th`

-to check free RAM space including total space

## `top`

-to check percentage memory and CPU utilization

## `du`

-to check disk utilization

## `df -h`

-to check filesystem available and disk space allocated

# System Information commands

## `hostname`

-to check the name of the machine

## `lscpu`

-to check cpu/core/thread info of the linux server

## `arch`

-to check the type of architecture of the system

## `lsblk`

-to see list of storage devices, disk partition on the linux server

## `uname -a`

-to see OS name of the linux server

# Process Management commands

## `ps -ef | grep <process>`

-to check if a process is running or not

## `pgrep <process>`

-to get PID of a process

## `kill -9 <PID>`

-to kill a process using PID

### Why use `kill` command when we can use `systemctl` command

Because `systemctl` command is only used for services not processes

## `pkill <process>`

-to stop a process using its name

## `jobs`

-to see all active jobs

## `bg`

-to resume a job in background

## `fg`

-to resume a job in foreground

## `nohup ./script >/dev/null &`

-to run a script in background

# Networking Information commands

## `ifconfig`

-to check IP of your machine

## `ping <URL_of_website>`

-to check if a server or website is accessible or not

## `telnet IP Port`

-to check if a IP:PORT is accessible and open or not

## `netstat -putan | grep <portNumber>`

-to check if a port is open or not on our server

## `traceroute <URL_of_website>`

-to check all hubs in network path to reach a website

## `reboot`

-to restart linux server

## `shutdown`

-to shutdown linux server

# User Management commands

## `useradd`

-to create a new user

## `passwd <userName>`

-to change the password for a user

## `groupadd <groupName>`

-to create a new group on linux server

## `id <userName>`

-to check UserID or GroupID of a user

## `userdel <userName>`

-to delete a user

## `groupdel <groupName>`

-to delete a group

## `usermod -G <groupName> <userName>`

-to change the group of a user

# Automation commands

## `at <time>`

-to schedule a script to run on particular date/time

## `atq`

-to check `at` command in queue

## `ls > <nameOfFile>`

-stores the files in the given file in a folder

## `pwd >> <nameOfFile>`

-stores of present working directory and updates them further
