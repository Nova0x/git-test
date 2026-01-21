

# 🧰 Git Complete Cheatsheet

From project setup to pull requests and daily workflows.

---

## 1. Setup & Configuration

### Set User Identity

```bash
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
```

### Default Editor

```bash
git config --global core.editor "vim"
```

### Check Configuration

```bash
git config --list
```

### Line Endings (macOS / Linux)

```bash
git config --global core.autocrlf input
```

---

## 2. Starting a Repository

### Initialize Repository

```bash
git init
```

### Clone Repository

```bash
git clone <url>
git clone <url> folder_name
```

### Repository Status

```bash
git status
```

---

## 3. Basic Workflow

### Stage Files

```bash
git add file.txt
git add .
git add src/
```

### Commit Changes

```bash
git commit -m "commit message"
```

### Add & Commit Together

```bash
git commit -am "commit message"
```

### View History

```bash
git log
git log --oneline
git log --graph --oneline
```

---

## 4. Staging & Undo

### Unstage Files

```bash
git restore --staged .
git restore --staged file.txt
```

### Discard Changes

```bash
git restore .
git restore file.txt
```

### Reset Commits

```bash
git reset --soft HEAD~1
git reset HEAD~1
git reset --hard HEAD~1
```

### Remove File From Tracking

```bash
git rm --cached file.txt
```

---

## 5. Branching

### Create Branch

```bash
git branch feature
git switch -c feature
```

### Switch Branch

```bash
git switch feature
git checkout feature
```

### List Branches

```bash
git branch
git branch -a
```

### Delete Branch

```bash
git branch -d feature
git branch -D feature
```

### Rename Branch

```bash
git branch -m new_name
```

---

## 6. Merging

```bash
git merge feature
git merge --abort
git merge --ff feature
git merge --no-ff feature
```

---

## 7. Rebase

```bash
git rebase main
git rebase -i HEAD~3
git rebase --abort
git rebase --continue
```

---

## 8. Remote Repositories

### Add Remote

```bash
git remote add origin <url>
```

### View Remotes

```bash
git remote -v
```

### Push

```bash
git push -u origin main
git push
```

### Pull & Fetch

```bash
git pull
git pull origin main
git fetch
```

---

## 9. Stash

```bash
git stash
git stash list
git stash apply
git stash pop
git stash clear
```

---

## 10. Tags

```bash
git tag v1.0
git tag -a v1.0 -m "version 1.0"
git push --tags
```

---

## 11. Inspecting

```bash
git diff
git diff --staged
git show <commit_hash>
git log file.txt
git blame file.txt
```

---

## 12. Ignoring Files

### Create `.gitignore`

```bash
touch .gitignore
```

### Common Rules

```gitignore
node_modules/
.env
*.log
dist/
```

---

## 13. Pull Request Workflow

```bash
git switch main
git pull

git switch -c feature/login
git add .
git commit -m "add login"
git push -u origin feature/login
```

After approval:

```bash
git switch main
git pull
git branch -d feature/login
```

---

## 14. Fixing Mistakes

```bash
git commit --amend -m "new message"
git add file.txt
git commit --amend --no-edit
git revert <commit_hash>
```

---

## 15. Daily Workflow

```bash
git pull
git status
git add .
git commit -m "work update"
git push
```

### Switch Task

```bash
git stash
git switch other-branch
git stash pop
```

---

## 16. Git States Model

Working Directory → Staging Area → Local Repository → Remote Repository

---

## 17. Useful Aliases

```bash
git config --global alias.st status
git config --global alias.co checkout
git config --global alias.br branch
git config --global alias.cm commit
git config --global alias.lg "log --oneline --graph"
```

---

## 18. Troubleshooting

```bash
git clean -n
git clean -f
git bisect start
git revert <commit_hash>
git push
```

---

