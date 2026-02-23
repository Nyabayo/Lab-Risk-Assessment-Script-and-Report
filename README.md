# System Audit Compliance Checker

This script is a simple **System Audit Compliance Checker** that performs basic checks to verify if certain system configurations meet predefined compliance standards. It checks the following areas:

1. **File Permissions on Sensitive Directories**
2. **Active User Sessions**
3. **Disk Space Utilization**

## Features

### 1. File Permissions on Sensitive Directories
- **Function:** `check_file_permissions()`
- **Purpose:** Checks if the file permissions of a sensitive directory (e.g., `/secure_data`) are restricted to the owner and not accessible by group or other users.
- **Compliance Check:** Ensures no "other" or "group" users have read, write, or execute permissions on the directory.

### 2. Active User Sessions
- **Function:** `check_active_sessions()`
- **Purpose:** Checks the number of active user sessions on the system.
- **Compliance Check:** Ensures there are no more than 5 active user sessions (compliance threshold). If there are more than 5 active sessions, it flags it as non-compliant.

### 3. Disk Space Utilization
- **Function:** `check_disk_space()`
- **Purpose:** Checks the disk space utilization of the root directory (`/`).
- **Compliance Check:** Ensures the disk usage does not exceed 80%. If the usage exceeds this threshold, it flags it as non-compliant.

## Installation

To run this script, simply clone or download the repository, and ensure you have Python 3.x installed on your machine.

```bash
git clone <repository_url>
cd <repository_directory>
