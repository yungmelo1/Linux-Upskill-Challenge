# Linux Upskill Challenge - Day 14: File Permissions & Ownership

## Key Commands

- `ls -l` – View file permissions
- `chmod` – Change file permissions
- `chown` – Change file ownership
- `chgrp` – Change file group

## Examples

- `chmod u+x file` – Add execute permission for user
- `chmod 754 file` – Numeric mode: rwxr-xr--
- `sudo chown user file` – Change owner
- `sudo chgrp group file` – Change group

## Notes

- Permissions: user | group | others
- Numeric codes: r=4, w=2, x=1 (e.g. 7 = rwx, 5 = r-x)

