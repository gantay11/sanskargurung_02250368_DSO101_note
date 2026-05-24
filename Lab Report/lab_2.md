## itle: Linux Command Exploration and Basic System Operations

# Aim:
To explore basic Linux commands and perform file, directory, system, and process management operations using the terminal.

# Objectives:
1.	To understand basic Linux terminal commands. 
2.	To perform file and directory management tasks. 
3.	To explore file viewing and searching techniques. 
4.	To execute networking and system information commands. 
5.	To understand process management in Linux. 

# Theory
Linux is an open-source OS which can be found in servers and cloud platforms. It comes with a CLI which allows you to work on your system directly.
There are basic Linux commands that enable you to perform actions such as navigation, working with files, managing processes, and network-related actions.

Key Concepts:
•	CLI (Command Line Interface): Text-based interaction with the OS. 
•	File System: Hierarchical structure of directories and files. 
•	Processes: Running programs in the system. 
•	Permissions: Control access to files and directories.
 
# Introduction
The open-source operating system Linux is very popular because of its efficiency, which enables it to provide great support in many areas of computer usage, including server administration, virtual machines, and software development environment. It uses a command-line interface, where users are able to interact with the system via certain commands.

In order to perform various operations such as file management, directory manipulation, process control, and system monitoring, one needs to learn how to use the appropriate commands. This is particularly crucial for system administrators and software developers.
In this lab we will examine some fundamental Linux commands and the way they help in manipulating system files, directories, processes, and system resources overall.

## Procedure and Commands

# Basic Navigation Task

Task No.	                 Command	Meaning / Explanation
1	cd Student_Lab 
    cd Linux	          - Changes directory step-by-step into specified folders.
2	cd ..	              - Moves one level up to the parent directory.
3	cd ../..	          - Moves two levels up in the directory hierarchy.
4	cd /	              - Navigates to the root directory (top-most level).
5	tree	              - Displays directory structure in a tree format.
6	clear	              - Clears the terminal screen.
7	pwd	                  - Shows the full path of the current directory.
8	ls -l                 - Lists files with detailed information (permissions, size, date).
9	ls -lh	              -Lists files with sizes in human-readable format (KB, MB).
10	ls /home	         - Lists files of a specific directory without changing location.
11	cd Stu<TAB>	          -Auto-completes directory/file names using the TAB key.
12	history	              - Displays previously executed commands.
13	!!	                  - Re-executes the last command.
14	cd -	             - Switches to the previous directory.
15	man ls	              - Opens the manual/help page for a command.

## Directory Management Task 

# Create Directory Structure
- mkdir -p Student_Lab/Linux Networking Programming
Meaning:
The mkdir command is used to create directories. The -p option allows creating parent and nested directories in one command, even if some directories do not already exist.

# Go Inside Directory
- cd Student_Lab/Linux
Meaning:
The cd (change directory) command is used to move into the specified directory.

# Create Subfolders
- mkdir commands scripts
Meaning:
This command creates two new directories named commands and scripts inside the current directory.

# Delete a Directory
- rm -r Programming
Meaning:
The rm -r command is used to delete a directory and all its contents recursively.

# File Management Task

Task 1: Create Files
- touch notes.txt, practice.txt
Meaning:
The touch command is used to create new empty files. If the file already exists, it updates the file’s timestamp.

Task 2: Copy and Rename Files
- cp notes.txt commands/
mv practice.txt linux_practice.txt
Meaning:
•	cp (copy) is used to duplicate a file into another location. 
•	mv (move) is used to rename a file or move it to a different location. 

Task 3: Move File
- mv linux_practice.txt scripts/
Meaning:
Moves the file linux_practice.txt into the scripts directory.
Additional File Management Commands (Extra for Better Marks)

Task 4: Delete a File
- rm notes.txt
Meaning:
The rm command deletes a file permanently from the system.

Task 5: Copy Multiple Files
- cp notes.txt linux_practice.txt commands/
Meaning:
Copies multiple files into a specified directory.

Task 6: View File Details
- ls -l
Meaning:
Displays detailed information about files such as permissions, owner, size, and modification date.

Task 7: Check File Type
- file notes.txt
Meaning:
Shows the type of file (e.g., text file, binary file).

Task 8: Display File Content
- cat notes.txt
Meaning:
Displays the contents of a file in the terminal.

Task 9: Count Words, Lines, Characters
- wc notes.txt
Meaning:
Displays the number of lines, words, and characters in a file.

Task 10: Create File with Content
- echo "Linux is powerful" > file1.txt
Meaning:
Creates a file and writes content into it. If the file exists, it overwrites the content.

Task 11: Append Content to File
- echo "It is widely used" >> file1.txt
Meaning:
Adds new content to the existing file without deleting the previous content.

Task 12: Rename Multiple Files (Basic)
- mv file1.txt file2.txt
Meaning:
Renames a file from file1.txt to file2.txt.

Task 13:Display File (3 Ways)
- cat notes.txt
- less notes.txt
- head notes.txt
Meaning:
•	cat displays the full content of the file. 
•	less shows the content page by page, useful for large files. 
•	head displays the first few lines of the file. 

## Searching Task (with Meaning)
I.	Search Word
grep "Linux" notes.txt
Meaning:
Searches for the word “Linux” inside the file and displays matching lines.

II.	Find .txt Files
find Student_Lab -name "*.txt"
Meaning:
Searches and lists all files with .txt extension inside the Student_Lab directory.

## Network Commands 

I.	Check Connectivity
- ping google.com
Meaning:
Checks whether the system can connect to google.com and measures network response time.

II.	Download File
- wget https://example.com/sample.txt
Meaning:
Downloads a file from the given URL and saves it to the current directory.

## System Information Task 
- uname -a
Meaning:
Displays detailed system information including kernel version.
- cat /etc/os-release
Meaning:
Shows information about the Linux operating system version.
- whoami
Meaning:
Displays the currently logged-in user.
- uptime
Meaning:
Shows how long the system has been running.

## Process Management Task 
- ps
Meaning:
Displays currently running processes.
- top
Meaning:
Shows real-time system processes and resource usage.
- kill <PID>
Meaning:
Stops a running process using its Process ID (PID).

## File Creation Task 

# Create File
- echo "Linux Practice Lab" > lab.txt
Meaning:
Creates a file named lab.txt and writes the given text into it.

# Append Line
- echo "This is an additional line" >> lab.txt
Meaning:
Adds a new line to the existing file without removing previous content.

# Display File
- cat lab.txt
Meaning:
Displays the content of the lab.txt file in the terminal.

## Conclusion
The practical involved the use of various Linux commands in order to learn about simple operations on Linux systems including navigation, files & directories manipulation, files viewing, searching, networking operations, system information and process management.

It was found out through hands-on experience that Linux commands are very easy and simple to use, but they are very effective when it comes to carrying out complex operations. It also enabled us to learn more about the practical usage of Linux commands in real-world situations like servers and cloud computing.

## References
1.	The Linux Foundation. (2025). Linux Documentation. Available at: https://www.linux.org/ 
2.	Shotts, W. E. (2019). The Linux Command Line: A Complete Introduction. No Starch Press. 
3.	Nemeth, E., Snyder, G., Hein, T. R., & Whaley, B. (2017). UNIX and Linux System Administration Handbook. Pearson. 
4.	GNU Project. (2025). GNU Core Utilities Manual. Available at: https://www.gnu.org/software/coreutils/ 
5.	Canonical Ltd. (2025). Ubuntu Documentation. Available at: https://help.ubuntu.com/

