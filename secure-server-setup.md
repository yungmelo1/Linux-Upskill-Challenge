# 🔐 Linux Secure Web Server Setup (Ubuntu)

This guide automates the setup of a hardened Ubuntu web server with SSH security, UFW firewall, Fail2Ban, and NGINX.

---

## 🚀 Setup Steps

1. **Create User & SSH Key Login**
```bash
adduser mamour && usermod -aG sudo mamour
mkdir -p /home/mamour/.ssh && chmod 700 /home/mamour/.ssh
nano /home/mamour/.ssh/authorized_keys  # Paste key
chmod 600 /home/mamour/.ssh/authorized_keys
chown -R mamour:mamour /home/mamour/.ssh

# 1. Create a new sudo user and add SSH key
adduser mamour
usermod -aG sudo mamour
mkdir /home/mamour/.ssh
chmod 700 /home/mamour/.ssh
nano /home/mamour/.ssh/authorized_keys  # paste your public key
chmod 600 /home/mamour/.ssh/authorized_keys
chown -R mamour:mamour /home/mamour/.ssh

# 2. SSH Hardening
nano /etc/ssh/sshd_config
# Set:
#   PermitRootLogin no
#   PasswordAuthentication no
#   Port 2222  (or any non-default)
systemctl restart ssh

# 3. Install updates & core packages
apt update && apt upgrade -y
apt install ufw fail2ban nginx unattended-upgrades curl htop -y

# 4. Setup UFW firewall
ufw allow 2222/tcp   # or your chosen SSH port
ufw allow 'Nginx Full'
ufw enable

# 5. Enable automatic security updates
dpkg-reconfigure --priority=low unattended-upgrades

# 6. Start NGINX Web Server
systemctl start nginx
systemctl enable nginx

# 7. Configure Fail2Ban
nano /etc/fail2ban/jail.local
# Example contents:
# [sshd]
# enabled = true
# port = 2222
# banaction = iptables-multiport
# maxretry = 3

systemctl restart fail2ban

# 8. Verify services
systemctl status nginx
systemctl status fail2ban
ufw status
