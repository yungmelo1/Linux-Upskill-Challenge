# Linux Upskill Challenge - Day 13: Disk Usage and Cleanup

## 🔍 Checking Disk Usage

Used the following command to view disk usage:

```bash
df -h

# To understand what’s taking up space:

du -sh /*

# Also used:

du -sh ~/.*  # To check hidden folders in home

#Cleaned up unused APT files:

sudo apt clean
sudo apt autoremove

#Checked size of APT cache before cleanup::

sudo du -sh /var/cache/apt

