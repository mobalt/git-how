---
tags:
  - fix/audit
---
# Overview
This tutorial explains how to undo changes from a specific past commit using Git's `revert` command and Lazygit's revert feature. Unlike other undo operations in Git, `revert` creates a new commit that undoes the changes made by a previous commit, keeping your project history intact.

# Lazygit

### Reverting a Commit in Lazygit

1. **Accessing the Commits Panel**:
   - Press `4` to open the [[4. Commits]] panel in Lazygit. This panel lists all your commits.

2. **Selecting the Commit to Revert**:
   - Use the `up`/`down` arrow keys to navigate through the list of commits.
   - Locate the commit you want to revert.

3. **Performing the Revert**:
   - Once you've selected the commit, press `t`.
   - Lazygit will create a new commit that undoes the changes made in the selected commit.
   - A new commit is added to your history, effectively reversing the changes. ![Pasted image 20230722132317.png]

### Finding a Specific Commit

4. **Searching for Commits**:
   - If you need to find a specific commit, use `/` to initiate a search.
   - Enter keywords or phrases to narrow down the list.

# Basic Terminal

### Reverting a Commit Using Git

1. **Identifying the Commit**:
   - First, find the commit you need to undo:
     - Use `git log` to view a list of recent commits.
     - For a more concise list, use `git log --oneline`.
     - To see detailed changes (patches), use `git log -p`.

2. **Executing the Revert**:
   - Revert using the commit's SHA hash or relative position:
     ```bash
     # Revert using the commit's SHA hash
     git revert BADHASH

     # Revert a commit that's 3 commits ago
     git revert HEAD~3
     ```
   - After running the revert command, an editor will open for you to edit the commit message of the new revert commit. Save and exit the editor once done.

# Explanation

### Understanding Git Revert

1. **How Git Revert Works**:
   - Git creates a reverse patch of the commit you're reverting. This patch is then applied as a new commit.
   - This new commit is the inverse of the changes made in the original commit, effectively undoing those changes.
   - The original commit remains in your history, preserving the project's history and ensuring transparency.

---

### Note on Git Revert

- Remember that `git revert` is a safe way to undo changes as it doesn't alter your project's history. This is especially important in collaborative environments where changing shared history can lead to conflicts.

### Further Enhancements

- [ ] Consider adding a demonstration or illustration showing how a reverse patch is created and applied. This can help users visualize the process and understand how `git revert` maintains the integrity of the commit history.
