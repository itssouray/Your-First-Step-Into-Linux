# User Management in Linux

## Introduction
Linux is a multi-user operating system, meaning multiple users can operate the system simultaneously. Proper user management is essential for security, resource control, and system organization.

### Key Files
- `/etc/passwd` – Stores basic user account details.
- `/etc/shadow` – Stores encrypted user passwords.
- `/etc/group` – Contains group information.
- `/etc/gshadow` – Stores secure group-related data.

## Creating Users

### Using `useradd` (Most Distributions)
```bash
useradd username                   # Creates user without home directory
useradd -m username                # Creates user with home directory
useradd -s /bin/bash username      # Specifies default shell
```

### Using `adduser` (Debian-Based)
```bash
adduser username                   # Interactive prompt for user info
```

## Managing Passwords
```bash
passwd username                    # Set or change a user’s password
```

### Password Policies
```bash
chage -M 90 username               # Set password to expire after 90 days
passwd -l username                 # Lock the user account
passwd -u username                 # Unlock the user account
```

## Modifying Users
```bash
usermod -l new_name old_name       # Change username
usermod -d /new/home -m username   # Change and move home directory
usermod -s /bin/zsh username       # Change login shell
```

## Deleting Users
```bash
userdel username                   # Delete user (keep home directory)
userdel -r username                # Delete user and home directory
```

## Working with Groups

### Creating a Group
```bash
groupadd groupname
```

### Adding Users to a Group
```bash
usermod -aG groupname username
```

### Viewing Group Memberships
```bash
groups username
```

### Changing Primary Group
```bash
usermod -g primarygroup username
```

## Sudo Access

### Adding to Sudo Group
```bash
usermod -aG sudo username          # Debian/Ubuntu
usermod -aG wheel username         # RHEL/CentOS
```

### Granting Specific Sudo Permissions
```bash
visudo
```

In the file, add:
```bash
username ALL=(ALL) NOPASSWD: /path/to/command
```
