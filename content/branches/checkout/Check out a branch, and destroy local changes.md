---
tags:
  - panel/3
  - fix/audit
---
# Introduction
This tutorial demonstrates how to forcefully check out a branch using Lazygit, resulting in the loss of all local changes. This is a useful technique when you need to quickly switch to a different branch and you're certain that the uncommitted changes in your current branch are unnecessary or can be discarded.

# Lazygit
Lazygit simplifies the process of discarding local changes and checking out a new branch. Here's how to do it:

1. Launch Lazygit in your repository.
2. Press `2` to access the **Branches** panel.
3. Navigate through the branch list using `↓`/`↑` keys or your mouse to highlight the branch you want to switch to.
4. To forcefully check out the selected branch and discard all local changes, press `F`. This is a destructive action and cannot be undone.
5. A confirmation prompt will appear to ensure you want to proceed with this action, as it will permanently delete your local changes.
6. Confirm your choice. Lazygit will then checkout the new branch, and all uncommitted changes in your current branch will be lost.

   - **Warning:** Be absolutely sure before using this command as it will irreversibly delete your uncommitted changes.

# Basic Terminal
In case you're using the basic terminal, here's how to achieve the same result:

1. To discard all local changes in your current branch, use the following Git command:
   ```bash
   git reset --hard
   ```
   This command resets the index and working tree. Any changes to tracked files in the working tree since the last commit are discarded.

2. Then, checkout the branch you want to switch to:
   ```bash
   git checkout <branch-name>
   ```

   - **Note:** As with the Lazygit approach, this method is irreversible. Use it with caution.

# Conclusion
Forcefully checking out a branch and discarding local changes is a powerful but potentially risky operation in Git. Lazygit provides a user-friendly interface to perform this action, but it's essential to use it with care to avoid unintentional loss of data. In the terminal, a combination of `git reset` and `git checkout` commands serves the same purpose. Always double-check before performing these actions to ensure you don't accidentally lose important work.
