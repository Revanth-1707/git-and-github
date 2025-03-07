
# Git Commands Cheat Sheet

This README provides a comprehensive list of Git commands with explanations. Use this as a reference to understand and use Git effectively.

---

## Table of Contents
1. [Setup and Configuration](#setup-and-configuration)
2. [Creating Repositories](#creating-repositories)
3. [Basic Snapshotting](#basic-snapshotting)
4. [Branching and Merging](#branching-and-merging)
5. [Sharing and Updating Projects](#sharing-and-updating-projects)
6. [Inspection and Comparison](#inspection-and-comparison)
7. [Debugging](#debugging)
8. [Patching](#patching)
9. [Advanced Commands](#advanced-commands)
10. [Aliases](#aliases)

---

## Setup and Configuration

### `git config`
Configure Git settings.

```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```

- `--global`: Applies the configuration to all repositories on your system.
- `--local`: Applies the configuration to the current repository only.

---

## Creating Repositories

### `git init`
Initialize a new Git repository.

```bash
git init
```

- Creates a `.git` directory in the current folder, turning it into a Git repository.

### `git clone`
Clone an existing repository.

```bash
git clone <repository-url>
```

- Downloads a copy of the repository to your local machine.

---

## Basic Snapshotting

### `git add`
Add files to the staging area.

```bash
git add <file>
git add .
```

- `<file>`: Adds a specific file to the staging area.
- `.`: Adds all changes in the current directory.

### `git commit`
Commit changes to the repository.

```bash
git commit -m "Your commit message"
```

- `-m`: Allows you to add a commit message directly.

### `git status`
Check the status of your working directory.

```bash
git status
```

- Shows which files are staged, unstaged, and untracked.

### `git diff`
Show differences between working directory and staging area.

```bash
git diff
```

- Use `git diff --staged` to see changes in the staging area.

---

## Branching and Merging

### `git branch`
List, create, or delete branches.

```bash
git branch
git branch <branch-name>
git branch -d <branch-name>
```

- `<branch-name>`: Creates a new branch.
- `-d`: Deletes a branch.

### `git checkout`
Switch branches or restore working tree files.

```bash
git checkout <branch-name>
git checkout -b <new-branch-name>
```

- `-b`: Creates and switches to a new branch.

### `git merge`
Merge branches.

```bash
git merge <branch-name>
```

- Merges the specified branch into the current branch.

### `git rebase`
Reapply commits on top of another base tip.

```bash
git rebase <branch-name>
```

- Use with caution, as it rewrites commit history.

---

## Sharing and Updating Projects

### `git pull`
Fetch and merge changes from a remote repository.

```bash
git pull origin <branch-name>
```

- Combines `git fetch` and `git merge`.

### `git push`
Upload local repository content to a remote repository.

```bash
git push origin <branch-name>
```

- Pushes commits to the specified branch on the remote.

### `git fetch`
Download objects and refs from another repository.

```bash
git fetch origin
```

- Fetches changes without merging them.

---

## Inspection and Comparison

### `git log`
Show commit history.

```bash
git log
```

- Use `git log --oneline` for a compact view.

### `git show`
Show information about a specific commit.

```bash
git show <commit-hash>
```

- Displays details of the specified commit.

### `git blame`
Show who last modified each line of a file.

```bash
git blame <file>
```

- Useful for tracking changes in a file.

---

## Debugging

### `git bisect`
Use binary search to find the commit that introduced a bug.

```bash
git bisect start
git bisect bad
git bisect good <commit-hash>
```

- Helps identify the exact commit causing an issue.

---

## Patching

### `git cherry-pick`
Apply changes from specific commits.

```bash
git cherry-pick <commit-hash>
```

- Applies the changes from the specified commit to the current branch.

---

## Advanced Commands

### `git stash`
Temporarily save changes.

```bash
git stash
git stash pop
```

- `stash`: Saves changes without committing.
- `pop`: Restores the most recently stashed changes.

### `git reset`
Reset the current HEAD to a specified state.

```bash
git reset --hard <commit-hash>
```

- `--hard`: Discards all changes in the working directory.

### `git reflog`
Show a log of all reference updates.

```bash
git reflog
```

- Useful for recovering lost commits or branches.

---

## Aliases

### Create custom Git aliases.

```bash
git config --global alias.co checkout
git config --global alias.br branch
```

- Example: Use `git co` instead of `git checkout`.

---

This README provides a solid foundation for understanding and using Git. For more advanced usage, refer to the [official Git documentation](https://git-scm.com/doc).

---

Feel free to contribute to this README by adding more commands or improving explanations!
