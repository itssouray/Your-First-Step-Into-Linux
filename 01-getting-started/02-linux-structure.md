# Core components of a Linux Machine

```plaintext
+----------------------------------------------------+
| User Applications (Vim, Docker, Apache, etc.)     |
+----------------------------------------------------+
| Shell (Bash, Zsh, Fish, etc.)                     |  
+----------------------------------------------------+
| System Libraries (glibc, libc, OpenSSL, etc.)     |  
+----------------------------------------------------+
| System Utilities (ls, grep, systemctl, etc.)      |  
+----------------------------------------------------+
| Linux Kernel (Process, Memory, FS, Network)       |  
+----------------------------------------------------+
| Hardware (CPU, RAM, Disk, Network, Peripherals)   |
+----------------------------------------------------+
```

## 1. Hardware Layer

- Physical devices such as CPU, RAM, hard drives, network cards, and I/O peripherals.
- Managed by kernel-level drivers to interface with software components.

## 2. Linux Kernel

The kernel sits at the core of the OS and directly interacts with hardware. It provides:

- **Process Scheduling** – Efficient multitasking and context switching.
- **Memory Allocation** – Manages physical and virtual memory.
- **Device Control** – Interfaces with hardware through drivers.
- **File System Access** – Handles data storage and retrieval operations.
- **Networking Stack** – Manages network connections and protocols.

## 3. System Libraries

- Provide reusable code that applications and the shell rely on.
- Examples include C standard libraries, encryption libraries, and data processing libraries.

## 4. System Utilities

- Core tools and commands used for system management and diagnostics.
- Examples: `ls`, `top`, `journalctl`, `systemctl`, `chmod`.

## 5. Shell

- Acts as a user interface to the kernel via command-line input.
- Translates commands into system calls.
- Popular shells: Bash, Zsh, Fish, Dash.

## 6. User Applications

- Programs installed by the user to perform specific tasks.
- Includes editors (Vim, VSCode), servers (Apache, Nginx), containers (Docker), etc.
