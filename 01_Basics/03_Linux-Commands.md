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
