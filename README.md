# 🗄️ Automated Backup Script (backup.sh)

## 📌 Project Overview
This project was developed as part of the **IBM Linux Final Project**.  
It automates the process of backing up sensitive files by creating a compressed archive of files that were modified within the last 24 hours.  

The backup script (`backup.sh`) eliminates human error, improves security, and saves time by automating daily backups.

---

## ⚙️ Features
- ✅ Validates input arguments (target and destination directories)  
- ✅ Checks if directories exist  
- ✅ Identifies files modified in the last 24 hours  
- ✅ Creates a `.tar.gz` archive with a timestamp  
- ✅ Moves the backup to the destination directory  
- ✅ Supports **cron automation** for daily scheduling  

---

## 🚀 Usage

### 1️⃣ Run Manually
```bash
./backup.sh /home/project/password_files /home/project/backups
````

### 2️⃣ From `/usr/local/bin/`

After copying the script into `/usr/local/bin/`, you can run it globally:

```bash
backup.sh /home/project/password_files /home/project/backups
```

---

## 📂 Directory Setup

Before running the script, create the directories:

```bash
mkdir -p /home/project/password_files
mkdir -p /home/project/backups
```

---

## 🕒 Cron Job Automation

To run the backup automatically:

1. Start cron service (only needed in the lab environment):

```bash
sudo service cron start
```

2. Edit the cron table:

```bash
crontab -e
```

3. Add the job (daily at midnight):

```
0 0 * * * /usr/local/bin/backup.sh /home/project/password_files /home/project/backups
```

4. Verify your cron jobs:

```bash
crontab -l
```

---

## 📷 Deliverables (for Peer-Review Project)

* **Screenshots** of completed tasks:

  * Code snippets (`backup.sh` sections for Tasks 1–13)
  * Script execution output
  * File permissions
  * Generated `.tar.gz` file
  * Cron job schedule
* **Completed backup.sh script**

---

## 🛠️ Tech Stack

* **Shell Scripting (Bash)**
* **Linux utilities**: `tar`, `date`, `cron`
* **Automation**: `crontab`, `sudo service cron`

---

## 🧑‍💻 Author

* **Mingma Moktan**
* Project: *IBM Linux Final Project – Automated Backup Script*