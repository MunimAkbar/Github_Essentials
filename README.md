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
```

---

## SETUP & INIT  
Initializing and cloning repositories:
```bash
git init              # Initialize an existing directory as a Git repository  
git clone [url]       # Clone an existing repository from remote  
```

---

## STAGE & SNAPSHOT  
Working with snapshots and the Git staging area:
```bash
git status                  # Show modified files in working directory  
git add [file]              # Stage a file for commit  
git add .                   # Stage all changes in current directory  
git reset [file]            # Unstage a file (keep changes)  
git diff                    # Show changes not staged  
git diff --staged           # Show staged changes not committed  
git commit -m "[message]"   # Commit staged content  
git commit -am "[message]"  # Stage & commit all tracked files  
```

---

## BRANCH & MERGE  
Isolating work in branches, changing context, and integrating changes:
```bash
git branch                  # List branches (* marks active branch)  
git branch [branch-name]    # Create a new branch  
git checkout [branch]       # Switch to a branch  
git checkout -b [branch]    # Create and switch to a new branch  
git merge [branch]          # Merge branch into current branch  
git log --oneline --graph   # Visualize commit history in a compact graph  
```

---

## INSPECT & COMPARE  
Examining logs, diffs, and object information:
```bash
git log                         # Show commit history  
git log --oneline               # Compact commit history  
git log branchB..branchA        # Commits on A not in B  
git log --follow [file]         # Show commits for a file (even after renames)  
git diff branchB...branchA      # Show differences between branches  
git show [SHA]                  # Show details of a commit/object  
```

---

## SHARE & UPDATE  
Working with remote repositories:
```bash
git remote -v                   # Show remote repositories  
git remote add [alias] [url]    # Add remote alias  
git fetch [alias]               # Fetch all branches from remote  
git merge [alias]/[branch]      # Merge remote branch into current branch  
git push [alias] [branch]       # Push local commits to remote branch  
git pull                        # Fetch and merge from remote  
git pull --rebase               # Rebase instead of merge when pulling  
```

---

## UNDOING CHANGES  
Fixing mistakes and cleaning up:
```bash
git checkout -- [file]          # Discard changes in file (restore last commit)  
git reset HEAD [file]           # Unstage a file (keep changes)  
git revert [commit]             # Create a new commit that undoes a previous one  
git reset --hard [commit]       # Reset branch to commit (discard all changes)  
git clean -fd                   # Remove untracked files and directories  
```

---

## TRACKING PATH CHANGES  
Versioning file removals and path changes:
```bash
git rm [file]                   # Delete file and stage removal  
git mv [old-path] [new-path]    # Rename/move file  
git log --stat -M               # Show logs with path changes  
```

---

## TEMPORARY COMMITS (Stash)  
Temporarily store modified files to switch branches:
```bash
git stash           # Save modified/staged changes  
git stash list      # List stashes  
git stash pop       # Apply and remove latest stash  
git stash apply     # Apply latest stash but keep it in stash list  
git stash drop      # Remove the latest stash  
```

---

## TAGGING  
Marking specific points in history (like releases):
```bash
git tag                            # List all tags  
git tag -a v1.0 -m "Version 1.0"   # Create an annotated tag  
git show v1.0                      # Show details of tag  
git push origin v1.0               # Push a specific tag to remote  
git push --tags                    # Push all tags to remote  
```

---

## REWRITE HISTORY  
Rewriting branches, updating commits, clearing history:
```bash
git commit --amend                 # Edit the last commit (message or content)  
git rebase [branch]                # Replay commits from current branch onto target  
git rebase -i HEAD~n                # Interactive rebase for the last n commits  
git reset --hard [commit]          # Reset to commit (erases history after commit)  
```

---

## IGNORING PATTERNS  
Preventing unintentional staging/committing of files:
```bash
git config --global core.excludesfile [file]   # Global ignore file  
```

Example `.gitignore` file:
```bash
logs/  
*.notes  
*.log  
node_modules/  
dist/  
.env  
```

---

## HELP  
Get help when you need it:
```bash
git help [command]     # Show help for a specific command  
git [command] --help   # Another way to get help  
```

---

✨ This cheatsheet summarizes the most commonly used Git commands.  
