# Understanding the Folder Structure

### Explanation of System Directories

user@hostname:/#

user@hostname:~$
 

~  -- /home/user
 

- **`:`** This colon separates the user/host information from the current working directory.
- **`/`** The forward slash represents the **root directory**, the top-level directory in the file system hierarchy.
- **`#`** The pound sign indicates that the user is the **root user** (the superuser with administrative privileges).
- **`$`** The dollar sign indicates that the user is a **normal, non-root user** with limited privileges.

### **Symbolic Links (Less Significant)**
| Directory | Description |
|-----------|-------------|
| `/sbin -> /usr/sbin` | System binaries for administrative commands (linked to `/usr/sbin`). |
| `/bin -> /usr/bin` | Essential user binaries (linked to `/usr/bin`). |
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
| `/home` | Default location for user home directories. |
| `/opt` | Used for installing optional third-party software. |
| `/srv` | Holds data for services like web servers (rarely used in containers). |
| `/root` | Home directory for the root user. |

### **Temporary & Volatile Directories**
| Directory | Description |
|-----------|-------------|
| `/tmp` | Temporary files (cleared on reboot). |
| `/run` | Holds runtime data for processes. |
| `/proc` | Virtual filesystem for process and system information. |
| `/sys` | Virtual filesystem for hardware and kernel information. |
| `/dev` | Contains device files (e.g., `/dev/null`, `/dev/sda`). |

### **Mount Points**
| Directory | Description |
|-----------|-------------|
| `/mnt` | Temporary mount point for external filesystems. |
| `/media` | Mount point for removable media (USB, CDs). |
| `/data` | Likely your **mounted volume** from Windows (`C:/ubuntu-data`). |
