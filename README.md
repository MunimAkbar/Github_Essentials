# Git Essentials Cheatsheet

A handy guide for commonly used Git commands, from setup to advanced operations.  

---

## SETUP  
Configuring user information used across all local repositories:

```bash
git config --global user.name "[firstname lastname]"   # Set your name for commit history
git config --global user.email "[valid-email]"         # Set your email for commits
git config --global color.ui auto                      # Enable command line coloring
git config --list                                      # View all Git configurations


SETUP & INIT

Initializing and cloning repositories:
git init              # Initialize an existing directory as a Git repository
git clone [url]       # Clone an existing repository from remote
