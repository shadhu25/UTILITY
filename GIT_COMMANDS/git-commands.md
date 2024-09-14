# Git Commands Cheat Sheet

---

## 1. Git Initialization and Status

```bash
git status
```
- Shows the current state of the working directory and the staging area.

```bash
git init
```
- Initializes the current folder as a Git local repository.

```bash
git add .
```
- Adds all files to the staging area.

```bash
git add one.txt
```
- Adds the file `one.txt` to the staging area.

---

## 2. Git Restore

```bash
git restore
```
- Restores the working tree files to their last committed state.

---

## 3. Git Commit

```bash
git commit
```
- Commits all files in the staging area without a commit message.

```bash
git commit -m "first commit"
```
- Commits all staged changes with the message "first commit."

```bash
git commit -am "second commit"
```
- Stages and commits all changes with the message "second commit."

---

## 4. Git Reset

```bash
git reset
```
- Moves all files from the staging area back to the working directory.

```bash
git reset index.html
```
- Unstages the file `index.html` without affecting its working directory changes.

```bash
git reset --hard 6t8h54
```
- Resets the repository to commit `6t8h54` and deletes all changes after that commit.

```bash
git reset --hard HEAD~5
```
- Resets the repository to 5 commits before the current HEAD, and deletes changes after that.

---

## 5. Git Revert

```bash
git revert 6t8h54
```
- Creates a new commit to reverse the changes made in commit `6t8h54`.

```bash
git revert HEAD~5
```
- Creates a new commit to reverse changes from 5 commits ago.

---

## 6. Git Log

```bash
git log
```
- Shows a list of all commits.

```bash
git log --oneline
```
- Shows a condensed log of commits with one line per commit.

---

## 7. Git Configuration

```bash
git config --list
```
- Lists all Git configuration settings.

```bash
git config --global user.email "Dummy@gmail.com"
git config --global user.name "Krishu"
```
- Sets global username and email for commits.

```bash
git config --global user.email
git config --global user.name
```
- Retrieves the global Git username and email.

```bash
git config user.email "Dummy@gmail.com"
git config user.name "Krishu"
```
- Sets local username and email for the current repository.

```bash
git config user.email
git config user.name
```
- Retrieves the local Git username and email.

```bash
git config global core.editor "code --wait"
```
- Sets VS Code as the default editor for Git.

---

## 8. Git Branching

```bash
git branch
```
- Lists all branches in the repository.

```bash
git branch nav
```
- Creates a new branch named `nav`.

```bash
git checkout nav
```
- Switches to the branch `nav`.

```bash
git checkout -b nav2
```
- Creates and switches to a new branch named `nav2`.

```bash
git switch nav
```
- Switches to the branch `nav`.

```bash
git switch -c nav2
```
- Creates and switches to a new branch named `nav2`.

```bash
git branch -M main
```
- Renames the current branch to `main`.

```bash
git branch -d nav
```
- Deletes the branch `nav`.

```bash
git checkout 5r4r5e
```
- Switches to the commit `5r4r5e`.

```bash
git checkout HEAD~3
```
- Switches to the commit 3 commits before the current HEAD.

```bash
git merge nav2
```
- Merges the branch `nav2` into the current branch.

---

## 9. Git Diff

```bash
git diff
```
- Shows the changes made to files that are not yet staged.

```bash
git diff --staged
```
- Shows the changes between the staged files and their previous versions.

```bash
git diff 87ght5 o8u6ty
```
- Compares the differences between two specific commits.

```bash
git diff 87ght..o8u6ty
```
- Compares the differences between two specific commits in a range.

```bash
git diff master..nav2
```
- Compares the differences between the `master` branch and the `nav2` branch.

---

## 10. Git Stash

```bash
git stash
```
- Temporarily saves changes without committing them.

```bash
git stash save "work in progress on X feature"
```
- Saves changes with a description for future reference.

```bash
git stash list
```
- Lists all saved stashes.

```bash
git stash pop
```
- Applies and removes the most recent stash.

```bash
git stash apply stash@{0}
```
- Applies the specified stash without removing it.

```bash
git stash apply stash@{0} <branch-name>
```
- Applies the stash to a specific branch.

```bash
git stash drop
```
- Removes a specific stash.

```bash
git stash clear
```
- Removes all stashes.

```bash
git reflog
```
- Shows a history of all actions, including those not part of `git log`.

---

## 11. Git Rebase

```bash
git rebase master
```
- Rebases the current branch onto the `master` branch.

```bash
git rebase --continue
```
- Continues the rebase after resolving conflicts.

---

## 12. Git Remote

```bash
git remote -v
```
- Shows all remote URLs associated with the repository.

```bash
git remote add origin url
```
- Adds a new remote named `origin` with the given URL.

```bash
git remote rename oldName newName
```
- Renames an existing remote.

```bash
git remote remove origin
```
- Removes the remote named `origin`.

---

## 13. Git Push, Pull, and Clone

```bash
git clone url
```
- Clones a remote repository into a new local directory.

```bash
git push origin main
```
- Pushes the `main` branch to the remote `origin`.

```bash
git push -u origin main
```
- Pushes the `main` branch and sets `origin` as the default upstream.

```bash
git pull origin main
```
- Fetches and merges changes from the `main` branch on the remote `origin`.

---

## 14. Miscellaneous

```bash
git --version
```
- Shows the Git version installed on your system.

```bash
extensions : git lens
```
- Useful Git extension for Visual Studio Code.

```bash
file .gitignore
```
- A file to specify which files or directories to ignore in a Git repository.
---
## 15. Multy Git Account Set Up
```bash 
config ram ram.pub sita sita.pub
```
- Shows public and private key in .ssh/  folder.

```bash
#Krishnkant47
Host ram.github.com
HostName github.com
PreferredAuthentications publickey
IdentityFile ~/.ssh/ram

#shadhu25
Host sita.github.com
HostName github.com
PreferredAuthentications publickey
IdentityFile ~/.ssh/sita

```
Set up for git in .ssh/config file for two accounts.

```bash
# account 1
git@ram.github.com:shadhu25/JavaScript.git
# account 2
git@sita.github.com:shadhu25/JavaScript.git

```
- remote url setup for above to git account.
