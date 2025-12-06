🔹 Title:

Linux Core-1 Module: Environment Variables & Shell Initialization Files

🔹 Objective:

Describe what the lab intended to teach.

🔹 Tasks Completed:

List tasks like:
        •       Created new file in /etc/profile.d/
        •       Modified PATH using export
        •       Used nano to edit system configuration files
        •       Understood shell initialization behavior

🔹 Commands Used:
        •       sudo nano /etc/profile.d/myvars.sh
        •       export PATH=$PATH:/new/path
        •       source /etc/profile

🔹 Issues Encountered:

Describe your mistake:

Attempted sudo chown 200 myfile.txt, realized this changed file ownership rather than applying setuid permissions.

🔹 Resolution:

Correct command: sudo chmod u+s myfile.txt

🔹 Key Takeaways:
        •       Difference between chmod vs chown
        •       Understanding octal vs symbolic permissions
        •       Setuid permissions and when they apply
        •       Editing system-level files safely

🔹 Reflection:

This lab helped me understand how environment variables persist across shells and how Linux controls privilege behavior via permissions.
