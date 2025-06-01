# Linux Upskill Challenge - Day 12: System Logs

## 🧠 Overview

Today's focus was exploring the `/var/log` directory, which contains key system log files.

---

## 📂 Key Logs Explored

### 1. syslog

```bash
less /var/log/syslog
tail -n 10 /var/log/syslog

#2 auth.log

less /var/log/auth.log
grep sudo /var/log/auth.log

#3. dpkg.log

less /var/log/dpkg.log
grep "install " /var/log/dpkg.log

#4. Rotated logs

ls -lh /var/log/*.gz
zcat /var/log/syslog.1.gz | less
zgrep sudo /var/log/auth.log.1.gz

