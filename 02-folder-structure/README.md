# Understanding the Folder Structure

| File System            | Description                                           |
| ---------------------- | ----------------------------------------------------- |
| **ext2 / ext3 / ext4** | Common Linux file systems (ext4 is most widely used). |
| **XFS**                | High-performance file system for large files.         |
| **Btrfs**              | Advanced features like snapshots and checksums.       |
| **tmpfs**              | Temporary memory-based file system.                   |
| **vfat / ntfs**        | Used for Windows partitions or USB drives.            |


### Explanation of System Directories

### **Symbolic Links (Less Significant)**
| Directory | Description |
|-----------|-------------|
| `/sbin -> /usr/sbin` | System binaries for administrative commands (linked to `/usr/sbin`). |
| `/bin -> /usr/bin` | Essential user binaries (commands like ls, cp, mv, cat). |
| `/lib -> /usr/lib` | Shared libraries and kernel modules (linked to `/usr/lib`). |

### **Important System Directories**
| Directory | Description |
|-----------|-------------|
| `/boot` | Stores files needed for booting the system (not relevant in containers). |
| `/usr` | Contains most user-installed applications and libraries. |
| `/var` | Stores logs, caches, and temporary files that change frequently. |
| `/etc` | Stores system configuration files. |

### **User & Application-Specific Directories**
| Directory | Description |
|-----------|-------------|
| `/home` | Personal directories for each user. (/home/irosh) |
| `/opt` | Used for installing optional third-party software.(e.g., custom apps) |
| `/srv` | Holds data for services like web servers (rarely used in containers)(web or FTP servers). |
| `/root` | Home directory for the root user. |

### **Temporary & Volatile Directories**
| Directory | Description |
|-----------|-------------|
| `/tmp` | Temporary files (cleared on reboot). |
| `/run` | Stores runtime information (like process IDs). |
| `/proc` | Virtual filesystem for process and system information. |
| `/sys` | Virtual filesystem for hardware and kernel information. |
| `/dev` | Contains device files (e.g., `/dev/null`, `/dev/sda`). |

### **Mount Points**
| Directory | Description |
|-----------|-------------|
| `/mnt` | Temporary mount point for external filesystems. |
| `/media` | Mount point for removable media (USB, CDs). |
| `/data` | Likely your **mounted volume** from Windows (`C:/ubuntu-data`). |
