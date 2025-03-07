
# Git Commands Cheat Sheet 📜  

A complete guide to using Git efficiently.  

## 📜 Table of Contents  

1. [🔧 Git Configuration](#-git-configuration)  
2. [📂 Initializing and Cloning](#-initializing-and-cloning)  
3. [📁 Working with Files](#-working-with-files)  
4. [🌿 Branching](#-branching)  
5. [🔄 Merging and Rebasing](#-merging-and-rebasing)  
6. [🚀 Remote Repositories](#-remote-repositories)  
7. [⏪ Undoing Changes](#-undoing-changes)  
8. [📦 Stashing Changes](#-stashing-changes)  
9. [🏷️ Tags](#️-tags)  
10. [🐞 Debugging Git Issues](#-debugging-git-issues)  
11. [🔎 Useful Git Commands](#-useful-git-commands)  

---

## 🔧 Git Configuration  

Before using Git, configure your user details.  

```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```

Check your Git configuration:  
```bash
git config --list
```

---

## 📂 Initializing and Cloning  

### Initialize a New Repository  
```bash
git init
```
Creates a new Git repository in the current directory.  

### Clone an Existing Repository  
```bash
git clone <repository-url>
```
Downloads a repository from GitHub or another remote source.  

---

## 📁 Working with Files  

### Check Status  
```bash
git status
```
Shows the status of the working directory and staging area.  

### Add Files to Staging Area  
```bash
git add <file-name>  # Add a specific file  
git add .  # Add all changes  
```
Stages files for commit.  

### Commit Changes  
```bash
git commit -m "Your commit message"
```
Saves changes to the local repository.  

### Remove Tracked Files  
```bash
git rm <file-name>
```
Deletes a file from the repository and working directory.  

---

## 🌿 Branching  

### List Branches  
```bash
git branch
```
Shows all local branches.  

### Create a New Branch  
```bash
git branch <new-branch-name>
```
Creates a new branch.  

### Switch Branch  
```bash
git switch <branch-name>
```
or  
```bash
git checkout <branch-name>
```
Switches to an existing branch.  

### Create and Switch to a New Branch  
```bash
git switch -c <new-branch-name>
```
or  
```bash
git checkout -b <new-branch-name>
```
Creates a new branch and moves to it.  

### Delete a Branch  
```bash
git branch -d <branch-name>  # Delete local branch  
git push origin --delete <branch-name>  # Delete remote branch  
```

---

## 🔄 Merging and Rebasing  

### Merge Branches  
```bash
git merge <branch-name>
```
Combines another branch into the current branch.  

### Rebase a Branch  
```bash
git rebase <branch-name>
```
Reapplies commits from one branch onto another.  

### Cherry-Pick a Commit  
```bash
git cherry-pick <commit-hash>
```
Applies a specific commit from another branch.  

---

## 🚀 Remote Repositories  

### Add a Remote Repository  
```bash
git remote add origin <repository-url>
```
Links a local repository to a remote repository.  

### View Remote Repositories  
```bash
git remote -v
```
Shows remote repository URLs.  

### Push Changes to Remote  
```bash
git push origin <branch-name>
```
Uploads local changes to GitHub.  

### Pull Changes from Remote  
```bash
git pull origin <branch-name>
```
Fetches and merges changes from the remote repository.  

### Fetch Changes without Merging  
```bash
git fetch
```
Downloads updates from the remote repository but does not apply them.  

---

## ⏪ Undoing Changes  

### Undo Last Commit (Keep Changes)  
```bash
git reset --soft HEAD~1
```
Moves the last commit back to staging.  

### Undo Last Commit (Remove Changes)  
```bash
git reset --hard HEAD~1
```
Deletes the last commit and changes.  

### Revert a Commit  
```bash
git revert <commit-hash>
```
Creates a new commit that undoes a previous commit.  

### Discard Changes in a File  
```bash
git checkout -- <file-name>
```
Resets a file to the last committed state.  

---

## 📦 Stashing Changes  

### Save Uncommitted Changes  
```bash
git stash
```
Stores uncommitted changes temporarily.  

### Apply Stashed Changes  
```bash
git stash pop
```
Applies and removes the last stashed change.  

### Show Stash List  
```bash
git stash list
```
Displays saved stashes.  

### Drop Stashed Changes  
```bash
git stash drop
```
Deletes a specific stash.  

---

## 🏷️ Tags  

### List Tags  
```bash
git tag
```
Displays all tags.  

### Create a Tag  
```bash
git tag -a v1.0 -m "Version 1.0"
```
Creates an annotated tag.  

### Push Tags  
```bash
git push origin --tags
```
Uploads all tags to the remote repository.  

---

## 🐞 Debugging Git Issues  

### Find a Bug using `git bisect`  
```bash
git bisect start
git bisect bad  # Mark the current (buggy) commit
git bisect good <commit-hash>  # Mark a known good commit
```
Git will check commits between good and bad to find the issue.  

Once the bad commit is found:  
```bash
git bisect reset
```

### View History of HEAD Changes  
```bash
git reflog
```
Shows a history of changes to HEAD, even if commits were reset.  

### Check for Merge Conflicts  
```bash
git diff --check
```
Lists potential merge conflicts before merging.  

### Find Who Made Changes to a Line  
```bash
git blame <file-name>
```
Shows the commit and author for each line of the file.  

### Show the Last Commit that Modified a File  
```bash
git log -p <file-name>
```

---

## 🔎 Useful Git Commands  

### Show Commit History  
```bash
git log --oneline --graph --decorate --all
```
Displays commit history in a visual format.  

### Check Differences  
```bash
git diff
```
Displays unstaged changes.  

---

This README provides a solid foundation for understanding and using Git. For more advanced usage, refer to the [official Git documentation](https://git-scm.com/doc).

---

Feel free to contribute to this README by adding more commands or improving explanations!
