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

## Objective
Learn how to manage software on Linux systems using package management tools. This module focused on installing, upgrading, and removing packages using `apt`, resolving dependencies, and investigating package details.

---

## Summary
Linux uses pre-compiled software packages that include binaries, configuration files, and dependency information. The APT package manager simplifies installing and upgrading software, handling most dependency issues automatically.

This module introduced working with repositories, installing packages from both remote sources and downloaded `.deb` files, fixing broken installations, upgrading systems, and cleaning up unused packages. I also learned how to prevent packages from being upgraded by placing them on hold.

---

## Tasks Completed
- Switched to the root user using `sudo -i`
- Updated package repositories
- Installed software packages from repositories
- Downloaded packages using `apt-get download`
- Installed `.deb` files using `dpkg -i`
- Fixed missing dependencies with `apt-get install -f`
- Upgraded packages using `apt-get upgrade` and `dist-upgrade`
- Removed unused software and configuration files
- Investigated package details
- Placed a package on hold with `apt-mark`

---

## Commands Used

```bash
sudo -i
apt-get update
apt-get install <package>
add-apt-repository
dpkg -i <file.deb>
apt-get download <package>
apt-get install -f
apt-get upgrade
apt-get dist-upgrade
apt-get remove <package>
apt-get purge <package>
apt-get clean
apt-get autoclean
apt-get autoremove
apt-cache show <package>
apt-mark hold <package>
apt-mark unhold <package>
```
---

## Key Concepts

### APT Sources
- Repositories are listed in `/etc/apt/sources.list`
- `apt-get update` refreshes package information
- Broken sources can cause installation errors

### Installing Software

#### From a repository
```bash
apt-get install <package>
apt-get download <package>
dpkg -i <file.deb>
apt-get install -f
apt-get upgrade
apt-get dist-upgrade
```
----
## Key Takeaways
- APT manages software installation, upgrades, and dependencies
- Missing dependencies can be fixed with `apt-get install -f`
- `apt-get upgrade` updates packages, while `dist-upgrade` also handles dependency changes
- `apt-get remove` and `apt-get purge` delete software, with purge removing configuration files
- Cleaning commands prevent the cache from growing out of control:
  - `apt-get clean`
  - `apt-get autoclean`
  - `apt-get autoremove`
- `apt-cache show <package>` displays package details
- Packages can be placed on hold to prevent unintended upgrades

---

## Reflection
This module hit me in a personal way because it explained so many things that confused me early in my Linux journey. When I first tried to learn Linux, I didn’t realize that different distributions used different package managers, different repositories, different dependencies — and that updates could break things if the right packages weren’t installed. I was trying to learn Linux while taking exams and working full-time, and I never had the time to sit down and understand what was actually happening under the hood.

Seeing how APT works finally made all of that make sense. Installing packages, fixing broken dependencies, and upgrading software showed me why things kept breaking before not because I was doing something wrong, but because Linux really does depend on matching the right packages and versions. This module made software management helped me understand why the distro you choose matters.

---


---

