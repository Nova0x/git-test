# Git Test


## This is about testing Git


GIT COMPLETE CHEATSHEET
From project start to pull request and daily workflows

---

1. SETUP AND CONFIG

---

Install identity
git config --global user.name "Your Name"
git config --global user.email "[you@example.com](mailto:you@example.com)"

Default editor
git config --global core.editor "vim"

Check config
git config --list

Line endings
git config --global core.autocrlf input

---

2. STARTING A REPOSITORY

---

Create new repo
git init

Clone existing repo
git clone <url>
git clone <url> folder_name

Check repo status
git status

---

3. BASIC WORKFLOW

---

Add files to staging
git add file.txt
git add .
git add src/

Commit changes
git commit -m "message"

Add and commit together
git commit -am "message"

View history
git log
git log --oneline
git log --graph --oneline

---

4. STAGING AND UNDO

---

Unstage files
git restore --staged .
git restore --staged file.txt

Discard local changes
git restore file.txt
git restore .

Reset last commit but keep files
git reset --soft HEAD~1

Reset last commit and unstage files
git reset HEAD~1

Hard reset and delete changes
git reset --hard HEAD~1

Remove file from tracking only
git rm --cached file.txt

---

5. BRANCHING

---

Create branch
git branch feature

Switch branch
git switch feature

Create and switch
git switch -c feature

Old style switch
git checkout feature

List branches
git branch
git branch -a

Delete branch
git branch -d feature
git branch -D feature

Rename branch
git branch -m new_name

---

6. MERGING

---

Merge branch into current
git merge feature

Abort merge
git merge --abort

Fast forward merge
git merge --ff feature

No fast forward merge
git merge --no-ff feature

---

7. REBASE

---

Rebase current on main
git rebase main

Interactive rebase
git rebase -i HEAD~3

Abort rebase
git rebase --abort

Continue rebase
git rebase --continue

---

8. REMOTE WORK

---

Add remote
git remote add origin <url>

View remotes
git remote -v

Push first time
git push -u origin main

Normal push
git push

Pull changes
git pull
git pull origin main

Fetch only
git fetch

---

9. STASH

---

Save work
git stash

List stashes
git stash list

Apply stash
git stash apply

Pop stash
git stash pop

Clear stashes
git stash clear

---

10. TAGS

---

Create tag
git tag v1.0

Annotated tag
git tag -a v1.0 -m "version 1.0"

Push tags
git push --tags

---

11. INSPECTING

---

Show changes
git diff
git diff --staged

Show commit
git show <hash>

File history
git log file.txt

Who changed lines
git blame file.txt

---

12. IGNORE FILES

---

Create ignore file
touch .gitignore

Example entries
node_modules/
.env
*.log
dist/

---

13. PULL REQUEST FLOW

---

Typical workflow

1. Update main
   git switch main
   git pull

2. Create feature branch
   git switch -c feature/login

3. Work and commit
   git add .
   git commit -m "add login"

4. Push branch
   git push -u origin feature/login

5. Open pull request on platform

6. After approval
   git switch main
   git pull
   git branch -d feature/login

---

14. FIXING MISTAKES

---

Change last commit message
git commit --amend -m "new message"

Add file to last commit
git add file
git commit --amend --no-edit

Revert commit
git revert <hash>

---

15. COMMON DAILY FLOW

---

Start day
git pull

Work cycle
git status
git add .
git commit -m "work"
git push

Switch task
git stash
git switch other
git stash pop

---

16. GIT STATES MODEL

---

Working directory
Staging area
Local repository
Remote repository

Commands move files between these areas

---

17. ALIASES USEFUL

---

git config --global alias.st status
git config --global alias.co checkout
git config --global alias.br branch
git config --global alias.cm commit
git config --global alias.lg "log --oneline --graph"

---

18. TROUBLESHOOT

---

Clean untracked files
git clean -n
git clean -f

Find bad commit
git bisect start

Undo pushed commit
git revert <hash>
git push

---

## END OF CHEATSHEET

Save this file as GIT_CHEATSHEET.txt for quick reference
