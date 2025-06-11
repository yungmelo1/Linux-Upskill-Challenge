# Linux Upskill Challenge - Day 20: File & Disk Usage

## Disk & Inode Usage
- `df -h` — Show disk usage (human-readable)
- `df -ih` — Show inode usage

## Folder & File Size
- `du -sh *` — Show sizes of files/folders in current dir
- `du -h --max-depth=1` — Folder sizes, 1 level deep
- `du -sh * | sort -h` — Sort files/folders by size

## Notes
- Use `df` to monitor disk space per partition (especially `/`, `/home`)
- Use `du` to find what’s taking up space
- Inodes matter if you hit file limits before size limits
