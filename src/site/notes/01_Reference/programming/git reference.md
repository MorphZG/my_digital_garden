---
{"dg-publish":true,"permalink":"/01-reference/programming/git-reference/","title":"Git and GitHub Reference Guide","tags":["linux","coding","configuration"]}
---


# Git and GitHub Reference Guide

A comprehensive guide to using Git and GitHub, ideal for quick reference.

---

## Table of Contents

[[01_Reference/programming/git reference#1. Basic Concepts\|#1. Basic Concepts]]
[[01_Reference/programming/git reference#2. Setup\|#2. Setup]]
[[01_Reference/programming/git reference#3. Common Git Commands\|#3. Common Git Commands]]
[[01_Reference/programming/git reference#4. Branching\|#4. Branching]]
[[01_Reference/programming/git reference#5. Merging and Rebasing\|#5. Merging and Rebasing]]
[[01_Reference/programming/git reference#6. Working with Remotes\|#6. Working with Remotes]]
[[01_Reference/programming/git reference#7. Stashing\|#7. Stashing]]
[[01_Reference/programming/git reference#8. GitHub Basics\|#8. GitHub Basics]]
[[01_Reference/programming/git reference#9. Pull Requests\|#9. Pull Requests]]
[[01_Reference/programming/git reference#10. Advanced Git Commands\|#10. Advanced Git Commands]]
[[01_Reference/programming/git reference#11. Tips and Best Practices\|#11. Tips and Best Practices]]

---

## 1. Basic Concepts

### What is Git?

Git is a distributed version control system, meaning each developer has a full copy of the project history on their local machine.

### What is GitHub?

GitHub is a web-based platform that hosts Git repositories, allowing for collaboration, pull requests, and additional tools.

---

## 2. Setup

1. Install Git: Download from [git-scm.com](https://git-scm.com/).
2. Configure Git:

   ```bash
   git config --global user.name "Your Name"
   git config --global user.email "your.email@example.com"
   ```

---

## 3. Common Git Commands

- Initialize a Repository:

  ```bash
  git init
  ```

- Clone a Repository:

  ```bash
  git clone <repository-url>
  ```

- Check Status:

  ```bash
  git status
  ```

- Add Files to Staging:

  ```bash
  git add <file>            # Add specific file
  git add .                 # Add all changes
  ```

- Commit Changes:

  ```bash
  git commit -m "Your commit message"
  ```

- Show Commit History:

  ```bash
  git log
  ```

- Undo Changes:

  ```bash
  git checkout -- <file>    # Discard changes in working directory
  git reset HEAD <file>     # Unstage a file
  ```

---

## 4. Branching

- Create a New Branch:

  ```bash
  git branch <branch-name>
  ```

- Switch Branches:

  ```bash
  git checkout <branch-name>
  ```

- Create and Switch to New Branch:

  ```bash
  git checkout -b <branch-name>
  ```

- Delete a Branch:

  ```bash
  git branch -d <branch-name>
  ```

---

## 5. Merging and Rebasing

- Merge Branches:

  ```bash
  git checkout <target-branch>
  git merge <source-branch>
  ```

- Rebase Branches:

  ```bash
  git checkout <feature-branch>
  git rebase <main-branch>
  ```

---

## 6. Working with Remotes

- Add a Remote Repository:

  ```bash
  git remote add origin <repository-url>
  ```

- View Remote Repositories:

  ```bash
  git remote -v
  ```

- Push Changes to Remote:

  ```bash
  git push origin <branch-name>
  ```

- Pull Changes from Remote:

  ```bash
  git pull origin <branch-name>
  ```

- Fetch Changes without Merging:

  ```bash
  git fetch origin
  ```

---

## 7. Stashing

- Stash Changes:

  ```bash
  git stash
  ```

- List Stashes:

  ```bash
  git stash list
  ```

- Apply Stash:

  ```bash
  git stash apply
  ```

- Apply and Drop Stash:

  ```bash
  git stash pop
  ```

---

## 8. GitHub Basics

- Create Repository:
  - Go to GitHub, click on "New," and follow the steps.

- Push an Existing Repo to GitHub:

  ```bash
  git remote add origin <repository-url>
  git push -u origin main
  ```

- Forking:
  - Click "Fork" on the GitHub repo page. This creates a copy of the repository in your account.

---

## 9. Pull Requests

1. Create a Pull Request:
   - Go to the GitHub repo page, select your branch, and click "New pull request."
2. Review and Merge:
   - Assign reviewers, add comments if necessary, and merge when ready.

---

## 10. Advanced Git Commands

- Revert a Commit:

  ```bash
  git revert <commit-hash>
  ```

- Interactive Rebase:

  ```bash
  git rebase -i <commit-hash>
  ```

- Cherry-pick a Commit:

  ```bash
  git cherry-pick <commit-hash>
  ```

- View Changes Since Last Commit:

  ```bash
  git diff
  ```

---

## 11. Tips and Best Practices

- Write Clear Commit Messages: Summarise changes and include details when necessary.
- Avoid Committing Large Files: Use `.gitignore` for files that don’t need to be tracked.
- Branch Often: Use branches for new features, bug fixes, or experiments.
- Pull Regularly: Sync with the main branch frequently to avoid merge conflicts.
- Squash Commits Before Merging: Combine small commits to keep history clean.

---

This guide should cover most basic and intermediate tasks you'll encounter with Git and GitHub. For more complex workflows or help with specific commands, refer to the [Git documentation](https://git-scm.com/doc).

```
