# Linux Upskill Challenge - Day 19: Inodes

Inodes are metadata containers for files. They store everything **except** the filename: permissions, ownership, timestamps, size, and data block pointers.

## 🔧 Key Commands

- `ls -i`: Show inode numbers for files.
- `ln file.txt hardlink.txt`: Create a **hard link** (shares the same inode).
- `ln -s file.txt symlink.txt`: Create a **symbolic link** (different inode).
- `find . -inum [inode]`: Find a file by its inode.
- `find . -inum [inode] -exec rm {} \;`: Delete by inode (advanced use).

## 🧪 Example

```bash
echo "inode demo" > file1.txt
ln file1.txt file1_link.txt
ln -s file1.txt file1_symlink.txt
ls -li file1*
