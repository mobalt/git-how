---
tags:
  - fix/audit
---
# Splitting a Commit

## Introduction
Splitting a commit in Git allows you to divide changes from a single commit into multiple smaller commits. This can be useful for improving clarity, managing the scope of changes, or refining your project's history. This guide covers how to split the last commit or a deeper commit in the history.

## Basic Terminal
### Splitting the Last Commit
1. **Undo the Last Commit:**
   ```bash
   git reset HEAD~
   # Retains changes in the working directory
   ```
2. **Stage Changes for the First New Commit:**
   ```bash
   git add <file1> <file2> <file3>
   # or
   git add -p <file> # for specific lines
   ```
3. **Create the First New Commit:**
   ```bash
   git commit -m "First commit"
   # or use your default editor
   ```
4. **Repeat Staging and Committing:**
   - Repeat for the second commit and any additional commits.
5. **Check for Uncommitted Changes:**
   ```bash
   git status # Should show no remaining changes
   ```
6. **Retrieve Stashed Changes (if any):**
   ```bash
   git stash pop
   ```

### Splitting a Deeper Commit
1. **Copy the SHA of the Commit to Split:**
   ```bash
   git log --oneline --graph
   ```
2. **Start an Interactive Rebase:**
   ```bash
   git rebase -i <commit-before-the-one-to-split>^
   ```
3. **Change Action to `edit` for the Target Commit:**
   ```
   edit 1f8f3f0 Commit you want to Split
   ```
4. **Undo the Commit to Split:**
   ```bash
   git reset HEAD~
   ```
5. **Stage and Commit the First Part:**
   ```bash
   git add <file1> <file2> <file3>
   git commit -m "First part of split commit"
   ```
6. **Repeat for Subsequent Parts:**
7. **Finalize with No Uncommitted Changes:**
   ```bash
   git status # Ensure no changes are left
   ```
8. **Continue the Rebase:**
   ```bash
   git rebase --continue
   ```
9. **Retrieve Stashed Changes (if any):**
   ```bash
   git stash pop
   ```

## Conclusion
Splitting a commit into multiple commits allows for a cleaner, more manageable history. This is a powerful technique in Git and can be particularly useful for organizing large commits into smaller, more understandable updates. Remember to be cautious when rewriting history, especially in shared branches or public repositories.
