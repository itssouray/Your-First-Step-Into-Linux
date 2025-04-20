# Understanding the Folder Structure

## Symbolic Links (Common Shortcuts)
| Directory         | Description                                                                 |
|------------------|-----------------------------------------------------------------------------|
| /sbin -> /usr/sbin | Administrative system commands (linked to /usr/sbin)                       |
| /bin -> /usr/bin   | Essential user command binaries (linked to /usr/bin)                       |
| /lib -> /usr/lib   | Shared libraries used by binaries and the system (linked to /usr/lib)      |

## Key System Directories
| Directory | Description                                                                 |
|-----------|-----------------------------------------------------------------------------|
| /boot     | Contains files required to boot the system (like kernel and bootloader)     |
| /usr      | Stores installed software, libraries, and documentation                     |
| /var      | Holds logs, spool files, and data that changes over time                    |
| /etc      | Configuration files for the operating system and applications               |

## User and Application Directories
| Directory | Description                                                                 |
|-----------|-----------------------------------------------------------------------------|
| /home     | Home directories for regular users (e.g., /home/saitama)                        |
| /opt      | Optional or third-party software installed manually                          |
| /srv      | Service-specific data (e.g., web server files), rarely used in containers    |
| /root     | Home directory for the root user                                             |

## Temporary and System Info Directories
| Directory | Description                                                                 |
|-----------|-----------------------------------------------------------------------------|
| /tmp      | Temporary files, cleared at reboot                                           |
| /run      | Runtime information for processes and system services                        |
| /proc     | Virtual filesystem exposing process and kernel details                       |
| /sys      | Interface to kernel and hardware-related information                         |
| /dev      | Device files representing hardware and virtual devices (e.g., /dev/null)     |

## Mount Points
| Directory | Description                                                                 |
|-----------|-----------------------------------------------------------------------------|
| /mnt      | Temporary mount location for filesystems (manual use)                        |
| /media    | Automatically mounted media (like USB drives, CDs)                           |
| /data     | Custom mount point, commonly used for shared or persistent data              |
