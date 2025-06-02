# Linux Upskill Challenge - Day 9: Aliases and Shell Prompt

## 🔄 Aliases

Today I created useful command shortcuts in my `~/.bashrc`:

```bash
alias ll='ls -la --color=auto'
alias gs='git status'
alias ..='cd ..'
alias update='sudo apt update && sudo apt upgrade'


These help me save time by shortening common commands.

I saved them by editing:

nano ~/.bashrc
source ~/.bashrc

I customized my shell prompt using:

export PS1="\[\e[0;32m\]\u@\h:\w$\[\e[m\] "
