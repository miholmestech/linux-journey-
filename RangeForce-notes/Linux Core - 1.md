# RangeForce – Linux Core Pathway

This file contains lab reflections and notes from the RangeForce Linux Core curriculum. Each module is documented with objectives, tasks, commands, takeaways, and personal reflections.

---

## Table of Contents
- [Module: CLI Introduction](#module-cli-introduction)
- [Module: Basic Linux File Editing](#module-basic-linux-file-editing)

---

# Module: CLI Introduction

> **Platform:** RangeForce – Linux Core Pathway 
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

> **Platform:** RangeForce – Linux Core Pathway  
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
