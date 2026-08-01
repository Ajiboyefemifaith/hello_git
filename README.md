# Hello-GIT
# Git & GitHub Cheat Sheet
*A Beginner's Practical Reference Guide*

---

# What is Git?

Git is a Version Control System (VCS).

Think of it as an unlimited "Undo" button for your project.

Git keeps a complete history of every change you make to your code, allowing you to:
- Go back to previous versions
- Collaborate with others
- Track who changed what
- Recover deleted files
- Experiment safely using branches

---

# What is GitHub?

GitHub is a cloud platform that stores Git repositories.

Git = Version Control
GitHub = Cloud Storage + Collaboration

Think of it like:

Microsoft Word = Git
OneDrive = GitHub

Git works without GitHub.

GitHub simply stores your Git repositories online.

---

# Git Workflow

Every project follows this lifecycle:

Working Directory
        │
        ▼
Staging Area
        │
        ▼
Commit (Local Repository)
        │
        ▼
GitHub (Remote Repository)

---

# Important Git Concepts

Repository (Repo)
A project managed by Git.

Working Directory
Your current project folder.

Staging Area
A temporary area where you prepare files before committing.

Commit
A permanent snapshot of your project.

Branch
A separate line of development.

Merge
Combining one branch into another.

Remote
The online repository (usually GitHub).

Clone
Download a repository from GitHub.

Push
Upload commits to GitHub.

Pull
Download changes from GitHub.

---

# Checking Git Installation

Check if Git is installed

```bash
git --version
```

Example Output

```
git version 2.xx.x
```

---

# Creating a Project

Create a folder

```bash
mkdir hello-git
```

Move into the folder

```bash
cd hello-git
```

Open VS Code

```bash
code .
```

---

# Initialize Git

Start tracking the project

```bash
git init
```

Creates a hidden folder:

```
.git
```

This folder stores:
- Commit history
- Branches
- Tags
- Configuration
- Entire project history

Never delete or edit it manually.

---

# Check Project Status

```bash
git status
```

Shows:

- Untracked files
- Modified files
- Staged files
- Branch name

This is the most frequently used Git command.

---

# Stage Files

Stage one file

```bash
git add app.py
```

Stage everything

```bash
git add .
```

Meaning:

"Prepare these files for the next commit."

---

# Commit Changes

```bash
git commit -m "Initial commit"
```

Example

```bash
git commit -m "Added customer recommendation model"
```

Think of a commit as a saved checkpoint.

---

# View Commit History

```bash
git log
```

Short version

```bash
git log --oneline
```

Shows all previous commits.

---

# Create a GitHub Repository

1. Login to GitHub
2. Click New Repository
3. Enter repository name
4. Leave it empty
5. Click Create Repository

---

# Connect Local Project to GitHub

```bash
git remote add origin https://github.com/username/project.git
```

Check remote

```bash
git remote -v
```

---

# Upload Project to GitHub

First push

```bash
git push -u origin main
```

Later pushes

```bash
git push
```

Meaning:

Upload commits from your computer to GitHub.

---

# Download Changes

```bash
git pull
```

Meaning:

Download the latest changes from GitHub.

Always pull before starting work.

---

# Clone a Repository

Download an existing repository

```bash
git clone https://github.com/username/project.git
```

Creates a copy on your computer.

---

# Branches

See branches

```bash
git branch
```

Create a branch

```bash
git branch feature-login
```

Create and switch immediately

```bash
git checkout -b feature-login
```

Switch branch

```bash
git checkout main
```

or

```bash
git switch main
```

---

# Merge Branch

Switch to main

```bash
git checkout main
```

Merge

```bash
git merge feature-login
```

Combines feature-login into main.

---

# Delete Branch

Delete local branch

```bash
git branch -d feature-login
```

---

# .gitignore

Create a file named

```
.gitignore
```

Example

```
ds_env/
__pycache__/
.env
*.db
*.csv
.idea/
.vscode/
```

Git ignores these files.

---

# Undo Commands

Unstage a file

```bash
git restore --staged app.py
```

Discard changes

```bash
git restore app.py
```

Undo last commit but keep files

```bash
git reset --soft HEAD~1
```

Undo last commit completely

```bash
git reset --hard HEAD~1
```

⚠ Use --hard carefully.

---

# Check Differences

Compare changes

```bash
git diff
```

Shows exactly what changed.

---

# Rename a Branch

```bash
git branch -m new-branch-name
```

---

# Remove Remote

```bash
git remote remove origin
```

---

# See Remote Repository

```bash
git remote -v
```

---

# Tag a Version

Create tag

```bash
git tag v1.0
```

Push tags

```bash
git push origin --tags
```

Useful for releases.

---

# Daily Professional Workflow

Start your day

```bash
git pull
```

Work on code

Check status

```bash
git status
```

Stage changes

```bash
git add .
```

Commit

```bash
git commit -m "Implemented recommendation engine"
```

Upload

```bash
git push
```

Done.

---

# Typical AI Project Workflow

```bash
git pull

# Write code

git status

git add .

git commit -m "Added customer embeddings"

git push
```

---

# Commit Message Examples

Good

```
Added login authentication

Implemented customer embeddings

Fixed recommendation bug

Improved dashboard UI

Refactored feature engineering pipeline

Updated README

Added CatBoost ranking model
```

Bad

```
Update

Stuff

Fix

Changes

Work
```

Always explain WHAT changed.

---

# Common Git Errors

"fatal: not a git repository"

Meaning:
You forgot to run

```bash
git init
```

or you are in the wrong folder.

---

"Everything up-to-date"

Meaning:
Nothing new to push.

---

"Merge conflict"

Meaning:
Two people changed the same lines.

Resolve the conflict manually.

Commit again.

---

"Permission denied"

Meaning:
Authentication problem.

Check GitHub login or SSH keys.

---

# Best Practices

✔ Commit often

✔ Use meaningful commit messages

✔ Pull before starting work

✔ Push after finishing work

✔ Never commit passwords

✔ Never commit API keys

✔ Use .gitignore

✔ Work on branches

✔ Merge only tested code

---

# Git Command Summary

| Command | Purpose |
|----------|----------|
| git init | Initialize Git repository |
| git status | Check project status |
| git add . | Stage all files |
| git add file.py | Stage one file |
| git commit -m "message" | Save snapshot |
| git log | View commit history |
| git log --oneline | Short history |
| git push | Upload changes |
| git pull | Download changes |
| git clone URL | Download repository |
| git branch | Show branches |
| git checkout branch | Switch branch |
| git checkout -b branch | Create and switch |
| git merge branch | Merge branch |
| git branch -d branch | Delete branch |
| git diff | Show file differences |
| git remote -v | Show GitHub connection |
| git restore file | Undo changes |
| git restore --staged file | Unstage file |
| git reset --soft HEAD~1 | Undo commit, keep files |
| git reset --hard HEAD~1 | Undo commit completely |

---

# The Golden Git Workflow

Write Code

↓

git status

↓

git add .

↓

git commit -m "Describe your work"

↓

git push

Repeat every day.
#### Git Lifecycle
Working Directory

↓

Staging Area

↓

Commit

↓

GitHub

## License 
MIT

## Author

Faith Ajboye-Femi