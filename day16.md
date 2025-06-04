# Linux Upskill Challenge - Day 16: Compression & Archiving

## Tools Covered

- `gzip` / `gunzip`: Fast compression, moderate ratio
- `bzip2` / `bunzip2`: Slower but higher compression
- `xz` / `unxz`: Higher compression ratio
- `tar`: Archive multiple files into one

## Commands

```bash
gzip file.txt         # Compress
gunzip file.txt.gz    # Decompress

bzip2 file.txt
bunzip2 file.txt.bz2

tar -cvf archive.tar file1 file2   # Create archive
tar -xvf archive.tar               # Extract

gzip archive.tar                  # Compress tarball to .tar.gz
gunzip archive.tar.gz && tar -xvf archive.tar
