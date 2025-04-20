# 💾 Disk and Storage Management in Linux (Made Easy)

Managing disks helps keep your Linux system fast and stable. Here's a simple guide to common tasks:

---

## 📊 Viewing Disk Info

1. **`lsblk`** – Shows all disks and partitions.  
   ➤ Great for a quick view of what's connected.

2. **`fdisk -l`** – Lists all disk partitions.  
   ➤ Use this to see detailed info.

3. **`blkid`** – Shows device UUIDs (used in mounting).

4. **`df -h`** – Shows how much disk space is used/free.  
   ➤ `-h` = human-readable (MB, GB).

5. **`du -sh /path`** – Shows size of a folder.  
   ➤ Example: `du -sh /var/log`

---

## 🧱 Partition Management

1. **`fdisk /dev/sdX`** – Create/manage partitions (for MBR).  
   ➤ Replace `sdX` with your disk (e.g., `sda`).

2. **`parted /dev/sdX`** – Similar to `fdisk` but supports GPT disks.

3. **`mkfs.ext4 /dev/sdX1`** – Format partition as ext4 (Linux default).

4. **`mkfs.xfs /dev/sdX1`** – Format as XFS (for large filesystems).

---

## 📂 Mounting and Unmounting

1. **`mount /dev/sdX1 /mnt`** – Mount the partition to `/mnt`.

2. **`umount /mnt`** – Unmount it.

3. **`mount -o remount,rw /mnt`** – Remount as read-write (useful for recovery).

---

## 📦 LVM (Logical Volume Manager)

Lets you manage storage more flexibly:

1. **`pvcreate /dev/sdX`** – Mark a disk for LVM use.

2. **`vgcreate vg_name /dev/sdX`** – Create a volume group.

3. **`lvcreate -L 10G -n lv_name vg_name`** – Create 10GB logical volume.

4. **`mkfs.ext4 /dev/vg_name/lv_name`** – Format the volume.

5. **`mount /dev/vg_name/lv_name /mnt`** – Mount it.

---

## 💤 Swap Management

1. **`mkswap /dev/sdX`** – Set up a swap partition.

2. **`swapon /dev/sdX`** – Enable the swap.

3. **`swapoff /dev/sdX`** – Disable the swap.

---

🧠 **Summary:**  
Use these commands to manage your disks, partitions, and memory. Always double-check disk names before running commands to avoid data loss!
