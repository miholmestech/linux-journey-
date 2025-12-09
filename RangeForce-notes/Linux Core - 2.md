# RangeForce – Linux Core Pathway

This file contains lab reflections and notes from the RangeForce Linux Core curriculum. Each module is documented with objectives, tasks, commands, takeaways, and personal reflections.

---
# Module 1: Linux User Management

> **Platform:** RangeForce – Linux Core 2 Pathway  
> **Date:** 12-08-2025

---
## Objective
Learn how to manage users and groups on a Linux system, including creating users, modifying accounts, removing users, and working with passwords. This module focused on acting as a supervisor with administrative control over system access.

---

## Summary
User management is a core responsibility of a system administrator. With elevated privileges, you can control who has access to the system, remove obsolete accounts, and secure the environment. This lab covered adding users, changing default shells, locking and unlocking accounts, and working with groups.

---

## Tasks Completed
- Connected to a server using SSH  
- Switched to the root user  
- Created a new user account  
- Viewed user IDs and account details  
- Modified a user’s default shell  
- Removed an existing user and home directory  
- Locked and unlocked passwords  
- Checked account status using `passwd -S`  
- Managed primary and secondary groups  

---
## Commands Used
```bash
adduser junior
getent passwd junior
usermod -s /bin/dash junior
id maria
deluser --remove-home maria
passwd -S anna
passwd -l anna
usermod -L anna
passwd -u angela
passwd -S angela
```
---

## Key Concepts

### User ID (UID)
- `0` → root (superuser)  
- `1–99` → system accounts  
- `100–999` → special/system uses  
- `1000+` → ordinary users (anna, junior)

### Shells
- User shells can be viewed with:
  
    getent passwd username

- Shells can be changed with:

    usermod -s /path/to/shell username

### Groups 
- Every user has a primary group
- Additional secondary groups provide access to shared resources
- Groups help organize users and permissions
  
---
## Key Takeaways
- User management is essential for system security
- `adduser`, `usermod`, and `deluser` are powerful administrative tools
- Locking unused accounts reduces the attack surface
- Accounts can be unlocked if access is needed again
- Groups help structure access and shared resources
  
---
## Reflection
This module made me feel like I had real control inside the terminal. Being able to add users, remove users, lock accounts, and view who belonged on the system felt powerful.
It wasn’t just typing commands it was making decisions about system access. I enjoyed seeing how much authority a system administrator has and how quickly the environment can be customized. This lab helped me understand the responsibility behind managing users and it made the terminal feel less abstract and more like a tool I could use with purpose. 

---

# Module 2: Linux Software Management

> **Platform:** RangeForce – Linux Core 2 Pathway  
> **Date:** 12-09-2025

---
