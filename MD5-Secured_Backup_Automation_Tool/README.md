# 🛡️ MD5-Secured Backup Automation Tool

## 📌 Project Overview
The **MD5-Secured Backup Automation Tool** is a Python-based, background surveillance and backup system. It intelligently scans designated directories, identifies new or modified files using **MD5 cryptographic checksums**, and creates timestamped, compressed archives. 

By implementing a "smart incremental backup" algorithm, this system ensures efficient data protection by preventing redundant data copying and optimizing storage space.

This project was developed as an Industrial Engineering Project, focusing on Python automation, file system manipulation, cryptography, and data integrity.

## 🚀 Core Features
* **Smart Incremental Backups:** Utilizes `hashlib.md5()` to compute file checksums, ensuring only newly added or genuinely modified files are transferred to the backup directory.
* **Automated Task Scheduling:** Runs continuously in the background at user-defined intervals via a Command Line Interface (CLI).
* **Automated Archiving:** Dynamically generates timestamped `.zip` files (e.g., `MarvellousBackup_2026-02-09_22-15-10.zip`) using Python's `zipfile` module with `ZIP_DEFLATED` compression.
* **Metadata & Structure Preservation:** Uses `os.walk()` and `shutil.copy2()` to accurately mirror complex, nested folder architectures and preserve critical file metadata, such as modification timestamps.

## 🛠️ Technical Stack
* **Language:** Python 3.x
* **Core Libraries:** `os`, `sys`, `time`, `shutil` (File & Directory Operations)
* **Cryptography:** `hashlib` (MD5 Checksums)
* **Compression:** `zipfile` (Archive Generation)
* **Automation:** `schedule` (Job Scheduling & Task Execution)

## ⚙️ System Architecture & Logic
The system is divided into five core modular functions:
1. **`main()`:** Parses command-line arguments (CLI) to capture the target backup directory and the execution interval. Handles user help and usage flags.
2. **`schedule.every().minutes`:** Triggers the backup cycle periodically. It utilizes `time.sleep()` to prevent the script from monopolizing CPU resources while waiting for the next cycle.
3. **`calculate_hash(path)`:** Reads files in 1024-byte binary chunks to efficiently compute a unique MD5 hash for change detection, handling large files gracefully.
4. **`BackupFiles(Source, Destination)`:** The core comparison engine. It compares hashes between the source and the backup destination. If the file is new or the hash mismatches, it executes a secure copy.
5. **`make_zip(folder)`:** Packages the newly updated backup folder into a single, highly portable `.zip` file for easy storage or cloud transfer.

## 💻 Usage & Execution

### Prerequisites
Ensure you have Python 3 installed. You will need to install the `schedule` library if it is not already in your environment:
```bash
pip install schedule