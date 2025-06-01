# Linux Upskill Challenge – Day 6: Understanding Linux Filesystem and Disk Usage

## 🧠 Overview

Today’s challenge was about exploring the Linux file system structure and learning to check disk and system information using essential commands.

---

## 📂 Key Commands and Learnings

### 🔹 Filesystem Hierarchy

```bash
cd /
ls -l

## 🔹 Check Disk Usage (df)
df -h

## 🔹 Directory Size (du)
sudo du -sh /var
sudo du -sh /var/*

🔹 Mounted Drives (mount, lsblk)
mount | column -t
lsblk

🔹 Kernel/System Info (uname)
uname -a
