
# SSH Server Hardening 🔒

## 📌 Overview
This project is part of Day 3 of the [Linux Upskill Challenge](https://github.com/livialima/linux-upskill-challenge).  
It demonstrates how to secure an SSH server on Ubuntu by:

- Disabling root login
- Enforcing key-based authentication
- Configuring the firewall to allow only SSH traffic

## 🧰 Tools Used
- OpenSSH
- UFW (Uncomplicated Firewall)
- Bash scripting

## 🛠️ Steps Performed
1. Edited `/etc/ssh/sshd_config` to:
   - Disable root login (`PermitRootLogin no`)
   - Disable password auth (`PasswordAuthentication no`)
2. Restarted the SSH service
3. Created UFW rules to allow only SSH (port 22)
4. Verified SSH status and firewall status

## 🚀 How to Run
```bash
sudo bash ssh_config_hardening.sh
