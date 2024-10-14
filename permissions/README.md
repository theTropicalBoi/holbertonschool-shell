# Shell Permissions

### Permissions in Linux
In Linux, file permissions control who can read, write, or execute a file or directory. There are three sets of permissions:
- **Owner (u)**: The user who owns the file.
- **Group (g)**: The group that owns the file.
- **Others (o)**: Everyone else.

Each file or directory has three types of permissions for each of these categories:
- **r (read)**: Allows reading the file.
- **w (write)**: Allows writing to or modifying the file.
- **x (execute)**: Allows executing the file (for scripts or binaries).


---
### Commands Related to Permissions
 - `chmod` *(Change mode)*
	- This command is used to change the permissions of a file or directory.
	- You can change permissions in symbolic notation (e.g., `u+x` to give the owner execute permissions) or using octal notation (e.g., `755`).
 - `sudo` *(Superuser do)*
	- Allows you to run commands with **root** (administrative) privileges.
	- Use this when you need higher-level permissions (e.g., installing software, modifying system files).
- `su` *(switch user)*
	- Allows you to switch to another user or to root.
 - `chown` *(Change owner)*
	- Changes the ownership of a file or directory to a different user.
- `chgrp` *(Change group)*
	- Changes the group ownership of a file or directory.
- `id` Displays the current user's ID, group ID, and group memberships.
- `groups` Displays the groups a user belongs to.
- `whoami` Prints the effective user ID (who you are logged in as).
- `adduser` or `useradd`: Used to create a new user.
- `addgroup`: Used to create a new group.

---
### Representing Permissions as a Single Digit
In octal notation, each permission set is represented by a digit:
- `r = 4`
- `w = 2`
- `x = 1`

So, the permissions `rwxr-xr--` translate to:
- Owner: `rwx` = 7 (4 + 2 + 1)
- Group: `r-x` = 5 (4 + 0 + 1)
- Others: `r--` = 4 (4 + 0 + 0)
