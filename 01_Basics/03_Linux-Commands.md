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
-creates a new terminal, to insert or edit data use 'I', to end editing use 'esc' and to save the file use 'SHIFT + :wq'

## `nano <fileName>`

-It works just like 'vi' but it is more advanced and helpful to beginners

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

## `sort <fileName>`

-to sort the content of the file

## `sort -r <fileName>`

-to sort the content of the file in reverse

## `sort <fileName> | uniq`

-to display unique content in the file

## `split -l <Number of splits> <fileName>`

-to split a file in certain different files
