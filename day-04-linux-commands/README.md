# Day 4 – Exploring Linux Command Tools and $PATH

## 🧠 What I Learned

Today I learned how Linux finds and executes commands using environment variables and lookup tools.

## 🔧 Key Commands

- `man <command>` – View manual pages (e.g. `man man`)
- `which <command>` – Shows path to command binary
- `type <command>` – Explains if it's an alias, keyword, or binary
- `whereis <command>` – Lists multiple binary and source locations
- `echo $PATH` – Shows the directories searched for commands
- Adding directories to `$PATH` via `export PATH=$PATH:/your/custom/path`

## 💡 Why This Matters

Understanding `$PATH` and how Linux finds executables is essential for scripting, troubleshooting, and system configuration in real-world server environments — especially for cloud engineering and DevOps.

## 🧪 Bonus

```bash
# Create a custom script and add to PATH
mkdir -p ~/bin
echo -e '#!/bin/bash\necho Hello from custom script!' > ~/bin/hello
chmod +x ~/bin/hello

# Temporarily add to PATH
export PATH=$PATH:~/bin

# Run it
hello# Day 04: Working with Linux Commands

## Key Topics Covered

1. **man**: Manual pages for Linux commands
2. **which**: Find the location of executables
3. **type**: Determine the type of command (e.g., alias, function, or binary)

## Why This Matters for Cloud Roles

Understanding these basic commands is crucial for cloud and DevOps roles, where you often need to quickly check available commands, locate executable paths, and explore command behaviors.

## Example Usage

### 1. **man (Manual Pages)**

The `man` command opens the manual for any Linux command.

Example:
```bash
man ls
