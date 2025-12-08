# RangeForce – Linux Core Pathway

This file contains lab reflections and notes from the RangeForce Linux Core curriculum. Each module is documented with objectives, tasks, commands, takeaways, and personal reflections.

---

<details>
<summary>Table of Contents</summary>

- [Module 1: CLI Introduction](#module-1-cli-introduction)
- [Module 2: Basic Linux File Editing](#module-2-basic-linux-file-editing)
- [Module 3: Linux File Management](#module-3-linux-file-management)
- [Module 4: Linux File Permissions and Ownership](#module-4-linux-file-permissions-and-ownership)
- [Module 5: Linux Environment Variables](#module-5-linux-environment-variables)
- [Module 6: Linux Execution Context](#module-6-linux-execution-context)
- [Module 7: Basic Shell Scripting](#module-7-basic-shell-scripting)
- [Module 8: Linux I/O Redirection](#module-8-linux-io-redirection)

</details>


---

# Module 1: CLI Introduction

> **Platform:** RangeForce – Linux Core 1 Pathway        
> **Date:** 12-01-2025

---

## Objective
Understand what a Command Line Interface (CLI) is, how it differs from a GUI, and how to use the terminal to navigate the Linux filesystem.

---

## Summary
A CLI allows users to interact with the computer using only the keyboard and commands. Unlike a graphical interface that relies on a mouse, the terminal provides powerful tools to accomplish tasks directly through text input. This module introduced the shell prompt and explained the role of commands.

---

## Tasks Completed
- Logged into a shell session  
- Identified the shell prompt  
- Ran basic commands to navigate the system  
- Viewed current working directory  
- Listed files and directories  

---

## Commands Used
```bash
ls
pwd
cd
cd ..
/var
```

---

## Directory Structure (FHS)
The **Filesystem Hierarchy Standard (FHS)** defines how Linux organizes files and directories. Key locations include:

- `/` – root of the filesystem  
- `/home` – user home directories  
- `/etc` – system configuration files  
- `/var` – variable data like logs  
- `/usr` – user tools and applications  

---

## Key Takeaways
- The terminal is efficient and powerful  
- Commands are small programs that perform tasks  
- You can navigate the system using keyboard only  
- `pwd` shows where you are, `ls` shows what's there  
- The shell prompt tells you when the system is ready  

---

## Reflection
This module helped me get comfortable using the terminal and navigating the filesystem without relying on a graphical interface. It set a solid foundation for the rest of the Linux Core path.

---

# Module 2: Basic Linux File Editing

> **Platform:** RangeForce – Linux Core 1 Pathway     
> **Date:** 12-02-2025

---

## Objective
Learn how to create, view, and edit files from the command line using `nano`, `cat`, and output redirection.

---

## Summary
This module introduced methods for working with files in Linux without a graphical editor. I practiced using the nano editor to create and update files, viewed file contents with cat, and used redirection operators to overwrite or append output to files. The exercises demonstrated how these tools fit into everyday Linux workflows.

---

## Tasks Completed
- Created and edited text files using `nano`  
- Viewed the contents of files  
- Appended and overwrote files using redirection  
- Combined multiple files into a new file  

---

## Commands Used
```bash
nano
cat
date
>
>>
```

---
## Concepts / Notes
- `nano filename` creates or opens a file for editing  
- `cat file` displays the content of a file  
- `>` overwrites a file with new output  
- `>>` appends new output to an existing file  

---

## Key Takeaways
- Terminal-based editing is fast and efficient for small changes
- Understanding > vs >> is important to avoid accidental overwrite
- Nano is simple, beginner-friendly, and widely available on Linux systems

---

## Reflection
This module helped me gain a better understanding of file editing on the command line. I enjoyed creating and modifying files. Redirecting output still feels strange, but I can tell it will get easier with more practice. I can already see how these skills will be useful for notes, logs, and quick edits while working in Linux.

---

# Module 3: Linux File Management

> **Platform:** RangeForce – Linux Core 1 Pathway        
> **Date:** 12-02-2025

---

## Objective
Learn how to create, remove, copy, rename, and find files and directories within the Linux filesystem.

---

## Summary
This module explained how to navigate the Linux filesystem and operate on files and directories. I practiced creating files and directories, removing them, copying and moving them, and searching for them using powerful command line tools. This is a foundational skill for working effectively in Linux.

---

## Tasks Completed
- Created files and directories  
- Removed files and directories  
- Copied and moved files and folders  
- Renamed files and directories  
- Searched for files using different criteria  
- Searched for text patterns within files  

---

## Commands Used
- `touch`  
- `mkdir`  
- `ls -l`  
- `rm` / `rm -r`  
- `rmdir`  
- `mv`  
- `cp` / `cp -r`  
- `find`  
- `grep -r`  

---

## Concepts / Notes

### Creating Files and Directories
- `touch filename` creates an empty file  
- `mkdir dirname` creates a directory  
- `ls -l` lists files in long format  

### Removing Files and Directories
- `rm file` removes a file  
- `rm -r dir` removes a directory with its contents  
- `rmdir dir` removes an **empty** directory  

> 💡 **-r is recursive. I need to remember this for deleting full directories.**

### Copying and Moving
- `mv source dest` moves or renames  
- `cp source dest` copies  
- `cp -r sourcedir dest` copies directories recursively  

### Finding Files and Directories
- `find /path -name "pattern"`  
- `find /path -type f` for files  
- `find /path -type d` for directories  
- `find /path -perm 644` for permissions  

### Searching Inside Files
- `grep pattern filename`  
- `grep -r pattern /path` searches recursively  

---

## Key Takeaways
- File and directory management is a core Linux skill  
- `touch` and `mkdir` create files and folders  
- `rm` removes files and `rm -r` removes directories  
- `mv` can move or rename  
- `cp -r` copies entire directory trees  
- `find` and `grep` are powerful tools for searching  

---

## Reflection
I feel more confident creating, modifying, and deleting files and directories. The part I struggle with is remembering to add `-r` when removing or copying directories. I know I will probably make this mistake in the future, but repetition will help. Every time I run into the problem, it will reinforce the habit. Learning these basics makes navigating Linux much easier and I can already see how these skills will help in real systems.


---

# Module 4: Linux File Permissions and Ownership 

> **Platform:** RangeForce – Linux Core 1 Pathway         
> **Date:** 12-03-2025

---

## Objective
Understand Linux file permissions and ownership, and learn how to grant, remove, and change permissions and ownership directly from the command line.

---

## Summary
This module covered the basics of Linux file permissions and ownership. I learned how to view and modify permissions using numerical and alphabetical formats, and how to change file ownership and group ownership with chown and chgrp. The exercises also introduced special permissions such as setUID, setGID, and the sticky bit.

---

## Tasks Completed
- Viewed permissions and ownership using `ls -l`  
- Changed permissions using numerical and alphabetical formats  
- Modified file ownership and group ownership  
- Assigned special permissions (setUID, setGID, sticky bit)  
- Used `sudo` when required to change ownership
  
---

## Commands Used
- `chmod`  
- `chown`  
- `chgrp`  
- `ls -l`  
- `sudo`

---

## Concepts / Notes

### File Permissions
- Three permission types:
  - `r` = read  
  - `w` = write  
  - `x` = execute  

- Three categories:
  - user (u)  
  - group (g)  
  - others (o)  

### Numerical Format
- `r = 4`, `w = 2`, `x = 1`
- Add numbers for each permission set:
  - example: `chmod 755 filename`

### Alphabetical Format
- **Who**
  - `u` = user  
  - `g` = group  
  - `o` = others  

- **What**
  - `+` = add permission  
  - `-` = remove permission  
  - `=` = set exact permission  

- **Which**
  - `r` = read  
  - `w` = write  
  - `x` = execute  

- `sudo` is required for changing owners or groups you do not belong to.

### Special Permissions
- **setUID (u+s / 4xxx)**  
Runs as the owner of the file.

- **setGID (g+s / 2xxx)**  
Runs as the group of the file.

- **Sticky bit (o+t / 1xxx)**  
Prevents users from deleting files they do not own in a shared directory.

---

## Key Takeaways
- Permissions can be set numerically or alphabetically  
- Numerical sets exact values, alphabetical adjusts existing ones  
- Ownership is separate from permissions  
- `sudo` is required to change the owner of a file  
- Special permissions (setUID, setGID, sticky bit) have specific behaviors  

---

## Reflection
I made a mistake during this module when trying to set special permissions. I mixed up `chown` and `chmod`, which changed the file owner instead of applying setUID. This error turned into a really helpful learning moment. It showed me that ownership and permissions are not the same thing, and they require different commands. Now that I understand the difference more clearly, I feel more confident that I can fix it whenever it comes up again.

---
# Module 5: Linux Environment Variables

> **Platform:** RangeForce – Linux Core 1 Pathway        
> **Date:** 12-03-2025

---

## Objective
Learn how to set, unset, promote, and demote shell and environment variables, and how to make environment variables persistent across sessions.

---

## Summary
This module introduced shell variables and environment variables, how they differ, and how they are used. I learned how to set and list variables, export them to child processes, unset them, and make them persistent through configuration files. I also practiced appending to the PATH variable and creating a configuration file in `/etc/profile.d`.

---

## Tasks Completed
- Listed shell and environment variables  
- Retrieved values using `set`, `printenv`, and `grep`  
- Created new shell and environment variables  
- Unset variables using `unset`  
- Promoted and demoted variables with `export`  
- Appended a path to the PATH variable  
- Created a persistent environment variable file in `/etc/profile.d`  

---

## Commands Used
- `set`  
- `set | more`  
- `set | grep`  
- `printenv`  
- `export`  
- `unset`  
- `nano`  
- `sudo`  

---

## Concepts / Notes

### Shell Variables
- Short-term: only exist in the current shell
- Not inherited by child processes
  
### Environment Variables
- Inherited by child shells and processes  
- Used to pass system information

Common examples:
- `SHELL`
- `USER`
- `HOME`
- `PWD`
- `OLDPWD`
- `PATH`
- `_` (last executed command)
  
### Persistent Environment Variables
To persist across shell sessions, use:

User-specific:
- `~/.bashrc`
- `~/.bash_profile`
- `~/.profile`

System-wide:
- `/etc/environment`
- `/etc/profile`
- `/etc/profile.d/*.sh`

---

## Tasks Completed
- Listed shell and environment variables
- Retrieved specific values with `grep` and `printenv`
- Created new shell variables
- Promoted variables to environment variables with `export`
- Demoted environment variables using `export -n`
- Unset variables using `unset`
- Appended a directory to the PATH variable
- Created a persistent environment variable file in `/etc/profile.d`

---

## Key Takeaways
- Shell variables are temporary; environment variables are inherited  
- `export` promotes shell variables to environment variables  
- `unset` removes variables  
- Persistent variables require editing user or system config files  
- Appending to PATH allows executables to be found from any directory  
- Nano is useful for creating configuration files  

---

## Reflection
This module required more attention, especially when creating a persistent environment variable in `/etc/profile.d`. I had to remember how to open and edit files in nano, and how to place the full export command inside the file. This actually took more time than I expected. One thing I really appreciate about the Linux Core Pathway in RangeForce is that if I truly get stuck and have exhausted all hints, they allow me to see the solution. I was never completely stuck. I could always eventually find an answer. This helped reinforce how environment variables work and why persistence matters. Working through this made me feel more comfortable with PATH, exporting variables, and using nano in real situations.

---
# Module 6: Linux Execution Context

> **Platform:** RangeForce – Linux Core 1 Pathway        
> **Date:** 12-04-2025

---

## Objective
Understand execution contexts in Linux, including users, systems, directories, privileges, and remote command execution.

---

## Summary
This module introduced how Linux runs commands based on which user is logged in, which system is being accessed, and which directory the shell is operating in. I learned how to identify the current user, host, and working directory, and how these affect file operations. The module also covered privileges, sudo usage, and how to execute commands on remote systems through SSH.

---

## Tasks Completed
- Used CLI to view system context  
- Identified current user with `whoami` and `id`  
- Viewed hostname and system identity  
- Navigated directories using `cd`, `pwd`, and path shortcuts  
- Observed prompt structure and execution context  
- Used `sudo` for elevated commands  
- Opened a privileged root session with `sudo -i`  
- Connected to remote systems using SSH  
- Executed remote commands, including privileged ones  

---

## Commands Used
- `whoami`
- `id`
- `hostname`
- `pwd`
- `cd`, `cd ..`, `cd ~`
- `sudo <command>`
- `sudo -i`
- `exit`
- `ssh user@server`
- `ssh user@server "<command>"`
---

## Concepts / Notes

### Execution Context
- Linux runs commands within a specific context:
  - which **user**
  - on which **system**
  - from which **directory**

### Command Prompt
Format:
- Execute a command remotely:
- Can combine with `sudo` for root tasks

---

## Key Takeaways
- Execution context depends on user, system, and directory
- The prompt shows username, hostname, and current path
- Always be aware of the current directory before running commands
- `sudo` grants temporary privileges for system tasks
- `sudo -i` opens a root session — use carefully
- SSH allows remote login and remote command execution

---

## Reflection
This module helped me understand how commands are affected by the user, system, and directory. It made me more aware of how important context is when running commands, especially when privileges are involved. I also practiced using both `sudo` and `sudo -i`, and I learned how to connect to remote systems with SSH. Being able to run commands on other machines from the terminal felt powerful, and I can see how this translates into real-world administration. 

---
# Module 7: Basic Shell Scripting

> **Platform:** RangeForce – Linux Core 1 Pathway        
> **Date:** 12-05-2025

---

## Objective
Learn how to write simple shell scripts, add execution permissions, pass arguments, and automate repeated tasks from the command line.

---

## Summary
This module introduced shell scripting as a way to automate repetitive command-line tasks. I learned how to write basic scripts, use arguments inside scripts, and make them executable. The assignment used a scenario where I worked at the “Sunset Library” and needed to create new library cards. Instead of typing the same commands repeatedly, writing a script simplified the task.

---

## Tasks Completed
- Created and executed simple shell scripts  
- Added the shebang (`#!/bin/sh`) to define the interpreter  
- Used `chmod +x` to make scripts executable  
- Ran scripts using `./script.sh`  
- Passed arguments into scripts (using `$1`, `$@`)  
- Automated the library card creation process with a custom script  

---

## Commands Used
- `echo`
- `chmod +x`
- `./script.sh`
- `#!/bin/sh`
- Shell arguments: `$1`, `$2`, `$@`

---

## Concepts / Notes

### What is a Shell Script?
- A text file containing shell commands
- Executed by the shell interpreter
- Used to automate tasks

### Shebang Line
- First line in a script: `#!`
- Declares the interpreter so the script runs like a binary
- Declares the interpreter so the script runs like a binary

  ### PATH Note
- Current directory is not in PATH by default  
- `./script.sh` tells the shell to execute from the working directory

---

### Automating Library Cards
- Final assignment: create a script that generates library cards and accepts the card ID as an argument  
- This saved time by avoiding repeated manual typing

---

## Key Takeaways
- Shell scripts automate repetitive commands  
- The shebang (`#!/bin/sh`) defines the interpreter  
- Scripts must be given execute permissions with `chmod +x`  
- Arguments allow scripts to change behavior dynamically  
- Using scripts reduces errors and saves time  

---

## Reflection
I really enjoyed this module because it made the idea of automation clear. The “Sunset Library” example helped me see how scripting saves time by avoiding repeated commands. It was fun to revisit “Hello world” and work with arguments like `$1` again — it reminded me of earlier modules and my command line book. Creating a script to generate library cards made the task feel realistic, and it helped me understand how scripts can be used in everyday system administration.

---
# Module 8: Linux I/O Redirection

> **Platform:** RangeForce – Linux Core 1 Pathway        
> **Date:** 12-05-2025

---

## Objective
Learn how standard streams work in Linux and how to redirect them, combine them, append to files, and use pipes, here documents, and here strings.

---

## Summary
This final module introduced how input and output streams work in Linux. I learned how to redirect standard output (stdout), standard error (stderr), and standard input (stdin) to files or other commands. I also learned how to use pipes to connect commands together, and how here documents and here strings feed input directly into commands. Even though it was a short module, it covered powerful concepts that are used constantly in real Linux work.

---

## Tasks Completed
- Identified standard streams (`stdin`, `stdout`, `stderr`)  
- Redirected `stdout` using `>`  
- Redirected `stderr` using `2>`  
- Redirected `stdin` using `<`  
- Appended output to files using `>>` and `2>>`  
- Combined output streams with `2>&1` and `&>`  
- Used pipes (`|`) to pass output between commands  
- Experimented with here documents (`<<`)  
- Used here strings (`<<<`) with commands  

---

## Commands Used
- `echo`
- `>` / `>>`
- `2>` / `2>>`
- `2>&1`
- `&>`
- `<`
- `|` (pipe)
- `<<` (here document)
- `<<<` (here string)
- `sort`, `cut`, `head`

---

## Concepts / Notes

### Standard Streams
- `stdin` (0) — standard input  
- `stdout` (1) — standard output  
- `stderr` (2) — standard error  

Output normally goes to the screen, but streams can be redirected.

---

## Key Takeaways
- Linux uses three standard streams:
  - `stdin` (input)
  - `stdout` (output)
  - `stderr` (errors)
- Streams can be redirected using:
  - `>` for output
  - `2>` for errors
  - `<` for input
- `>>` appends to a file instead of overwriting
- `2>&1` sends stderr to the same destination as stdout
- Pipes (`|`) connect commands together
- Here documents (`<<`) can send multiple lines of text into a command
- Here strings (`<<<`) send a single string into a command
- Order of redirection matters because bash evaluates from left to right

---

## Reflection
This module was short but very valuable. I finally understood how standard streams work and why redirecting them is so powerful. I want to revisit `2>&1` because combining streams seems important and I want to make sure I use it confidently. Pipes were especially interesting — I liked seeing how different commands can be connected to produce a result. Even though this was the last module in Core 1, it gave me a strong foundation for working with output and redirection in Linux.

---



