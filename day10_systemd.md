# Linux Upskill Challenge - Day 10: Systemd and Services

## 🧠 Overview

Today’s focus was on understanding how Linux boots and manages services using `systemd`. Explored how to list, enable, disable, and restart services.

---

## 🧾 What I Did

### 🧩 1. Verified systemd as PID 1:

```bash
ps 1


#2. Checked system uptime and last boot

uptime
who -b

#3. listed running services:

systemctl list-units --type=service


#4. Inspected and controlled the cron service:

systemctl status cron
sudo systemctl stop cron
sudo systemctl start cron
sudo systemctl restart cron
systemctl is-enabled cron
sudo systemctl disable cron
sudo systemctl enable cron


#5. Viewed previous boot log after reboot:

sudo reboot
journalctl -b -1



# Reflections
#Today clarified how the Linux system boots and how to manage services with systemctl. I'm more comfortable inspecting, restarting, and enabling/disabling services now.
