# RangeForce – Linux Core Pathway

This file contains lab reflections and notes from the RangeForce Linux Core curriculum. Each module is documented with objectives, tasks, commands, takeaways, and personal reflections.

---

## Table of Contents
- [Module: CLI Introduction](#module-cli-introduction)
- [Module: Basic Linux File Editing](#module-basic-linux-file-editing)

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
> **Date:** 12-01-2025

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
> **Date:** 12-02-2025

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
