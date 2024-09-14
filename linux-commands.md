### Command 1: `ls` (List Sub-directories)
```bash
# Lists all directories and files in the current directory
ls

# Lists all directories and files in the specified directory
ls [dir-path]  # Example: ls /shadhu/Download/photo/

# Lists all directories and files in the root directory
ls /

# Lists all directories and files in the home directory
ls ~

# Lists all directories and files in the parent directory
ls ..

# Lists all directories and files in long format
ls -l

# Lists all directories and files including hidden files
ls -a

# Lists all directories and files in long format, including hidden files
ll or ls -al

# Saves the output of the ls command to the specified file
ls -lS > [file-name]  # Example: ls -lS > ram.txt

# Lists all files with a specific pattern
ls *.*

# Lists all files with a specific file extension
ls *.file-extension  # Example: ls /Home/Document/*.html

# Lists only directories of the current directory
ls -d */

# Lists files and directories of each directory
ls */

# Lists almost all directories and files except implied . and ..
ls -A

# Displays sizes in human-readable format
ls -hl

# Lists directories and files sorted by size
ls -S

# Sorts directories and files alphabetically
ls -X

# Sorts files by time, newest first
ls -t

# Reverses the order while sorting
ls -r

# Lists files in long format, without showing the owner
ls -g

# Lists files in long format, without group information
ls -o

# Recursively lists subdirectories
ls -R
```

### Command 2: `cd` (Change Directories)
```bash
# Changes to the root directory
cd /

# Changes to the home directory
cd or cd ~

# Changes to the parent directory
cd ..

# Changes to the specified directory
cd [dir-path]  # Example: cd /shadhu/Download/photo/

# Changes to a directory with a white-space in its name
cd ["dir-name with white-space"]  # Example: cd "my book"
```

### Command 3: `cat` (Concatenate Files and Print)
```bash
# Displays input back to the terminal
cat

# Displays the content of the specified file
cat [file-name]  # Example: cat text.txt

# Displays the content of multiple files
cat [file-name1 file-name2 ...]  # Example: cat file1.txt file2.txt

# Displays file with line numbers for non-blank lines
cat -b [file-name]

# Displays file with line numbers for all lines
cat -n [file-name]

# Removes multiple blank lines, displaying only one
cat -s [file-name]

# Displays a file, marking end of non-blank lines with '$'
cat -E [file-name]

# Redirection: Overwrites or creates a new file with input
cat > [file-name]

# Redirection: Appends input to the specified file
cat >> [existing-file-name]

# Overwrites the content of one file into another
cat [file1-name ...] > [file2-name]

# Appends the content of one file to another
cat [file1-name ...] >> [file2-name]
```

### Command 4: `mkdir` (Make Directory)
```bash
# Creates a directory
mkdir [dir-name]  # Example: mkdir shadhu

# Creates multiple directories at once
mkdir {f1,f2,f3}

# Creates a subdirectory within existing directories
mkdir [existing-dir1/existing-dir2/new-dir]

# Creates multiple child directories within existing directories
mkdir [existing-dir1/existing-dir2/{f1,f2,f3}]

# Creates parent and child directories simultaneously
mkdir -p [new-dir1/new-dir2/{f1,f2,f3}]

# Creates multiple directories with subdirectories
mkdir -p {parent1,parent2}/{child1,child2}
```

### Command 5: `rm` and `rmdir` (Remove Directory)
```bash
# Removes an empty directory
rmdir [dir-name]  # Example: rmdir shadhu

# Removes empty nested directories
rmdir -p [dir1/dir2/dir3]

# Removes empty nested directories with verbose output
rmdir -pv [dir1/dir2/dir3]

# Removes directories with all contents recursively
rm -rv [dir1/dir2] or [parent-dir]
```

### Command 6: `cp` (Copy)
```bash
# Copies a file to another file
cp [file1] [file2]

# Copies multiple files into a directory
cp [file1 file2 ... dir]

# Copies files into a directory, asking for confirmation if files exist
cp -i [file1 file2 ... dir]

# Copies only the content of a directory into another directory
cp -R [dir1] [dir2]
```

### Command 7: `mv` (Move)
```bash
# Moves or renames a file
mv [file1] [file2]

# Moves multiple files into a directory
mv [file1 file2 ... dir]

# Moves a directory into another directory
mv [dir1] [dir2]

# Moves a directory and renames it
mv [dir1] [new-dir2]
```

### Command 8: `less` (View File Contents)
```bash
# Opens a file to view content one page at a time
less [file-name]

# Use arrow keys for scrolling, 'space' for page down, 'b' for page up, 'q' to quit
```

### Command 9: `touch` (Create/Update Files)
```bash
# Creates an empty file
touch [file-name]

# Updates the timestamp of the specified file
touch [existing-file-name]
```

### Command 10: `top` (Process Viewer)
```bash
# Displays all currently running processes
top

# Press 's' to change refresh delay, 'k' to kill a process by PID, 'q' to quit
```

### Command 11: `kill` (Terminate Processes)
```bash
# Kills a process by its PID
kill [pid]

# Finds the PID of a process by name
pidof [process-name]
```

### Command 12: `chmod` (Change File Permissions)
```bash
# Grants permissions to users for a file or directory
chmod [user-types][+ or -][permission-type] [file-name]  # Example: chmod oug+x text.txt

# Gives permission using numeric values
chmod [value] [file-name]  # Example: chmod 701 text.txt
```
### command-14 : `which`
```bash
# 'which' command provides the path of the given command/executable.
which [keyword] ->  this will give some information about the given keyword like its path {which cat}

# 'whatis' command provides a short description of the given command/executable.
whatis [keyword] -> this will give a short description of the given keyword {whatis cat}
```
### command-15 : `useradd`(create user)
```bash     
# Create a new user with the specified username.
useradd [user-name] -> creates a user with a name provided by the user {useradd krishn}

# Create a new user with a home directory.
useradd -m [user-name] -> creates a user with a name provided by the user and creates a default home directory for the new user {useradd krishn}

# Create a new user with a specified shell.
useradd [user-name] -s [shell-path] -> creates a user with a specified name and allows the user to use a particular shell {useradd krishn -s /bin/bash}

# Create a new user and assign them to an existing group.
useradd [user-name] -g [existing-group] -> creates a user and assigns them to an existing group {useradd krishn -g shadhu}

# Create a new user with a comment describing the user.
useradd [user-name] -c ["user-comment"] -> creates a user with a comment {useradd krishn -c "I am a new user here for coding work"}
```
### command-16 : `userdel`(delete user)
```bash
# Delete a user from the system.
userdel [user-name] -> delete the specified user {userdel krishn}

# Delete a user and their home directory/data.
userdel -r [user-name] -> delete the specified user and all of their data {userdel -r krishn}
```
### command-17 : `groupadd`(create group)
```bash
# List all groups connected to the current user.
groups -> list all the groups that are connected to the current user {groups krishn}

# List all the existing groups on the system.
cat /etc/group -> list all the groups that exist

# Create a new group.
groupadd [group-name] -> create a new group {groupadd shadhu}

# Delete an existing group.
groupdel [group-name] -> delete the specified group {groupdel shadhu}

# Add a user to a specific group.
gpasswd -a [user-name] [group-name] -> adding a user to the group {gpasswd -a krishn shadhu}

# Remove a user from a group.
gpasswd -d [user-name] [group-name] -> deleting a user from the group {gpasswd -d krishn shadhu}
```
### command-18 : `watch`
```bash
# Repeatedly run a command and refresh the output in real time.
watch [other-command] -> it will refresh the given command repeatedly {watch df -h}

# Set a time interval for refreshing the command output.
watch -n [sec] [other-command] -> it will refresh the command repeatedly and change the interval time {watch -n 5 df -h}
```
### command-19 : `head`
```bash
# Display the first 10 lines of a file.
head [file-name] -> print the first 10 lines of the file {head text.txt}

# Display the first n lines of a file.
head -[n] [file-name] -> print the first n lines of the file {head -5 text.txt}

# Display the first 10 lines and continuously update the file.
head -f [file-name] -> print the first 10 lines and update the file {head -f text.txt}
```
### command-20 : `tail`
```bash
# Display the last 10 lines of a file.
tail [file-name] -> print the last 10 lines of the file {tail text.txt}

# Display the last n lines of a file.
tail -[n] [file-name] -> print the last n lines of the file {tail -5 text.txt}

# Display the last 10 lines and continuously update the file.
head -f [file-name] -> print the last 10 lines and update the file {head -f text.txt}
```
### command-21 : `find`
```bash
# Find a file by name in a specified directory.
find [existing-dir-name] -name [file-name] -> find the given file in the directory and provide its absolute path {find /shadhu/krishn -name text.txt}

# Find a file with an unknown extension in a specified directory.
find [existing-dir-name] -name [file-name-without-extension] -> find the given file with an unknown extension and give its absolute path {find /shadhu/krishn -name text.*}

# Find files based on their extension.
find [existing-dir-name] -name [only-extension-of-the-file] -> find files in the directory by their extension {find /shadhu/krishn -name *.txt}

# Find files starting with specific letters in a directory.
find [existing-dir-name] -name [starting-letters-of-file] -> find the file by its starting letters {find /shadhu/krishn -name text1*}

# List all files created a specified number of days ago.
find [existing-dir-name] -mtime -[day] -> list all files created within the specified days {find /shadhu/krishn -mtime -2}
```
### command-22 : `wc`(word count)
```bash
# Display the number of lines, words, and characters in a file.
wc [file-name] -> list the total number of lines, words, and characters in the file {wc text.txt}

# Display the total number of characters in a file.
wc -c [file-name] -> list the total number of characters in the file {wc -c text.txt}

# Display the total number of lines in a file.
wc -l [file-name] -> list the total number of lines in the file {wc -l text.txt}

# Display the total number of words in a file.
wc -w [file-name] -> list the total number of words in the file {wc -w text.txt}

# Display the length of the longest line in a file.
wc -L [file-name] -> list the total number of characters in the longest line of the file {wc -L text.txt}
```
### command-23 : `cal`(calender)
```bash      
# Display the current month.
cal -> print the current month

# Display the current month in a transposed layout.
ncal -> transpose the output of the 'cal' command

# Display the calendar for a specific year.
cal [year] -> print all months of the specified year {cal 2016}

# Display the calendar for a specific month and year.
cal [month-num] [year] -> print the specified month of the specified year {cal 4 2016}

# Display the previous, current, and next month of the current year.
cal -3 -> print previous, current, and next months of the current year
```
### command-24 : `date`
```bash
# Display the current date and time.
date -> print the current date

# Set the system date and time.
date -s ["m/d/y h:m:s"] -> set the system date and time {date -s "11/20/2003 12:48:00"}

# Display the date in a custom format.
date +%d%h%y -> print the date in the specified format {output= 04jan17}

# Display the date with a custom format using hyphens.
date "+%d-%h-%y" -> print the date in a custom format {output= 04-jan-17}

# Display the date with a custom format using slashes.
date "+%d/%h/%y" -> print the date in a custom format {output= 04-jan-17}

# Display both date and time with a custom format.
date "+DATE: %m/%d/%y%nTIME: %H:%M:%S" -> print both the date and time with a custom format
# Example output:
# DATE: 01/04/17
# TIME: 22:25:13
```
