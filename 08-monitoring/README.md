# 🖥️ Linux System Monitoring

## 📌 Introduction

Monitoring your Linux system is crucial for maintaining performance, diagnosing issues, and ensuring the health of your infrastructure. With the right tools, you can easily track CPU usage, memory consumption, disk activity, network connections, and system logs in real time.

This guide introduces commonly used commands for system monitoring, along with explanations and examples to help you understand how to use them effectively.

---

## 🧭 Index of Commands Covered

### 🧠 CPU & Memory Monitoring
- `top` – Real-time overview of system processes and resource usage
- `htop` – Interactive and user-friendly version of `top`
- `vmstat` – Summarized view of system performance
- `free -m` – Shows available and used memory

### 💾 Disk Monitoring
- `df -h` – Displays disk space usage of all mounted file systems
- `du -sh /path` – Shows size of a specific directory
- `iostat` – CPU and disk I/O statistics

### 🌐 Network Monitoring
- `ip a` – Show network interfaces and IP addresses
- `netstat -tulnp` – View open ports and active network connections
- `ss -tulnp` – Faster, more modern alternative to `netstat`
- `ping` – Check network connectivity
- `traceroute` – Track the path to a remote host
- `nslookup` – DNS query tool for resolving domain names

### 📄 Log Monitoring
- `tail -f /var/log/syslog` – Follow live system log updates
- `journalctl -f` – View live logs on systems using `systemd`
- `dmesg | tail` – Show recent kernel log messages

---

## 🧠 CPU and Memory Monitoring

### `top` – Real-Time System Overview
Displays a live list of processes and resource usage.
```bash
top


Key columns:
- `PID`: Process ID
- `%CPU`: CPU usage
- `%MEM`: Memory usage

> Press `q` to quit.

---

### `htop` – Enhanced Process Viewer (requires installation)
More interactive than `top`, supports mouse and keyboard navigation.

```bash
htop
```
- Arrow keys: Navigate
- `F9`: Kill a process
- `F10`: Exit

Install with:
```bash
sudo apt install htop        # Debian/Ubuntu
sudo yum install htop        # RHEL/CentOS
```

---

### `vmstat` – System Performance Snapshot
Provides information about CPU, memory, and I/O.

```bash
vmstat 1 5
```
> Updates every 1 second, displays 5 updates.

---

### `free -m` – Check Memory Usage
Shows memory stats in megabytes.

```bash
free -m
```
Key info:
- `total`: Total RAM
- `used`: Currently used RAM
- `available`: RAM available for new processes

---

## 💾 Disk Monitoring

### `df -h` – Disk Space Usage
Displays space usage for mounted file systems in human-readable format.

```bash
df -h
```
Focus on:
- `/`: Root filesystem
- `Use%`: Disk space used

---

### `du -sh /path` – Directory Size
Shows size of a specific directory.

```bash
du -sh /var/log
```
Options:
- `-s`: Summary only
- `-h`: Human-readable (KB, MB, GB)

---

### `iostat` – CPU & Disk I/O Stats
Displays average CPU load and I/O stats.

```bash
iostat
```

Install with:
```bash
sudo apt install sysstat
```

---

## 🌐 Network Monitoring

### `ip a` – View Network Interfaces
Lists network devices and IP addresses.

```bash
ip a
```

---

### `netstat -tulnp` – Open Ports and Services
Shows active listening ports and associated programs.

```bash
netstat -tulnp
```
Flags:
- `-t`: TCP
- `-u`: UDP
- `-l`: Listening
- `-n`: Numeric IPs
- `-p`: Process name and PID

> Install if missing:
```bash
sudo apt install net-tools
```

---

### `ss -tulnp` – Socket Stats (Faster Alternative)
Quickly view sockets, ports, and associated processes.

```bash
ss -tulnp
```

---

### `ping` – Test Connectivity
Checks if a host is reachable.

```bash
ping google.com
```
> Press `Ctrl + C` to stop.

---

### `traceroute` – Trace Network Path
Shows the route taken by packets to a remote host.

```bash
traceroute google.com
```

> Install if needed:
```bash
sudo apt install traceroute
```

---

### `nslookup` – DNS Resolution Lookup
Displays domain name system records.

```bash
nslookup example.com
```

---

## 📄 Log Monitoring

### `tail -f` – Live View of Logs
Continuously watches log file output in real-time.

```bash
tail -f /var/log/syslog
```

---

### `journalctl -f` – Systemd Live Logs
Live system logs for distros using `systemd`.

```bash
journalctl -f
```

---

### `dmesg | tail` – Kernel Logs
View recent kernel messages from the ring buffer.

```bash
dmesg | tail
```

---