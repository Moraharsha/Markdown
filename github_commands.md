# VS Code + GitHub Complete Command Cheat Sheet

## 1. Check Git Installation

```bash
git --version
```

Displays the installed Git version.

---

## 2. Configure Git (First Time Only)

### Set Username

```bash
git config --global user.name "Your Name"
```

Example:

```bash
git config --global user.name "Vardhan Mora"
```

### Set Email

```bash
git config --global user.email "yourmail@example.com"
```

Example:

```bash
git config --global user.email "vardhan@gmail.com"
```

### Verify Configuration

```bash
git config --list
```

---

# Creating a New Repository

## 3. Navigate to Project Folder

```bash
cd path/to/project
```

Example:

```bash
cd D:\Projects\auth-service
```

---

## 4. Initialize Git Repository

```bash
git init
```

Creates a local Git repository.

---

## 5. Check Repository Status

```bash
git status
```

Shows:

- Modified files
- New files
- Deleted files
- Staged files

---

## 6. Add All Files

```bash
git add .
```

Stages all files.

### Add Single File

```bash
git add filename.java
```

Example:

```bash
git add AuthController.java
```

---

## 7. Commit Changes

```bash
git commit -m "Initial commit"
```

Example:

```bash
git commit -m "Added authentication module"
```

---

# Connecting to GitHub

## 8. Add Remote Repository

```bash
git remote add origin https://github.com/username/repository.git
```

Example:

```bash
git remote add origin https://github.com/vardhan/auth-service.git
```

---

## 9. Verify Remote Repository

```bash
git remote -v
```

Example Output:

```bash
origin https://github.com/vardhan/auth-service.git (fetch)
origin https://github.com/vardhan/auth-service.git (push)
```

---

## 10. Push Code First Time

```bash
git push -u origin main
```

or

```bash
git push -u origin master
```

depending on branch name.

---

## 11. Push Future Changes

```bash
git push
```

---

# Download Existing Repository

## 12. Clone Repository

```bash
git clone https://github.com/username/repository.git
```

Example:

```bash
git clone https://github.com/vardhan/auth-service.git
```

---

## 13. Move into Cloned Repository

```bash
cd auth-service
```

---

# Pull Latest Changes

## 14. Download Latest Changes

```bash
git pull
```

---

## 15. Pull Specific Branch

```bash
git pull origin main
```

---

# Branch Commands

## 16. View Current Branch

```bash
git branch
```

Current branch has:

```bash
*
```

Example:

```bash
* main
```

---

## 17. Create New Branch

```bash
git branch feature-auth
```

---

## 18. Switch Branch

```bash
git checkout feature-auth
```

---

## 19. Create and Switch Branch

```bash
git checkout -b feature-auth
```

---

## 20. Switch Back to Main

```bash
git checkout main
```

---

## 21. View All Branches

```bash
git branch -a
```

---

## 22. Delete Branch

```bash
git branch -d feature-auth
```

Force delete:

```bash
git branch -D feature-auth
```

---

# Merging Branches

## 23. Merge Feature Branch

Switch to main first:

```bash
git checkout main
```

Merge:

```bash
git merge feature-auth
```

---

# Undo Operations

## 24. Remove Staged File

```bash
git reset filename
```

Example:

```bash
git reset AuthController.java
```

---

## 25. Unstage Everything

```bash
git reset
```

---

## 26. Discard Changes

```bash
git checkout -- filename
```

Example:

```bash
git checkout -- application.properties
```

---

## 27. Reset Last Commit (Keep Files)

```bash
git reset --soft HEAD~1
```

---

## 28. Delete Last Commit Completely

```bash
git reset --hard HEAD~1
```

⚠️ Dangerous

---

# Git History

## 29. View Commit History

```bash
git log
```

---

## 30. Compact Commit History

```bash
git log --oneline
```

Example:

```bash
8f1e123 Added JWT Authentication
c7e921a Initial Commit
```

---

# Stashing

## 31. Save Current Changes Temporarily

```bash
git stash
```

---

## 32. View Stashes

```bash
git stash list
```

---

## 33. Restore Stash

```bash
git stash pop
```

---

# Remove Repository Connection

## 34. Remove Remote Repository

```bash
git remote remove origin
```

---

# Useful VS Code Terminal Commands

## Open Current Folder in VS Code

```bash
code .
```

---

## Open Specific Folder

```bash
code D:\Projects\auth-service
```

---

## Open Specific File

```bash
code application.properties
```

---

# Common Daily Workflow

## Step 1

```bash
git pull
```

## Step 2

Make changes

## Step 3

```bash
git add .
```

## Step 4

```bash
git commit -m "Implemented Product Service"
```

## Step 5

```bash
git push
```

---

# Complete New Project Workflow

```bash
git init

git add .

git commit -m "Initial commit"

git remote add origin https://github.com/username/project.git

git branch -M main

git push -u origin main
```

---

# Most Frequently Used Commands

```bash
git status

git add .

git commit -m "message"

git push

git pull

git clone <repo-url>

git branch

git checkout -b branch-name

git merge branch-name

git log --oneline

git remote -v
```

---

# VS Code + GitHub Interview Quick Notes

- Git = Version Control System
- GitHub = Cloud hosting for Git repositories
- Repository (Repo) = Project storage
- Commit = Snapshot of code
- Branch = Independent development line
- Merge = Combine branches
- Clone = Download repository
- Push = Upload local code to GitHub
- Pull = Download latest code from GitHub
- Remote = Connection to GitHub repository
- Origin = Default remote repository name
