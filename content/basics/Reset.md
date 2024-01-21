---
tags:
  - panel/4
  - fix/audit
---
# Introduction
Understanding how to reset commits in Git is crucial for managing your project's history. This guide covers the process of resetting commits in Lazygit and explains the different types of resets: soft, mixed, and hard.

# Lazygit
1. **Navigating to Previous Commits:**
   - Open Lazygit and navigate to the commit you want to reset to. This commit should be one before the commits you need to reset.
   - Use the `g` key to initiate the reset process.

2. **Reset Options:**
   - Upon pressing `g`, a menu with reset options will appear:
     - **Soft Reset (`soft`):** This option will uncommit changes but keep them staged. It's useful when you want to amend the commit without losing the work done.
     - **Mixed Reset (`mixed`):** This will uncommit and unstage your changes, but the changes will still be there in your working directory. It's helpful when you want to redo the staging.
     - **Hard Reset (`hard`):** This completely undoes the commit and deletes all changes. Use this with caution as it permanently removes the work done in those commits.


3. **Selecting a Reset Type:**
   - Choose the appropriate reset type based on your need. Remember, 'hard' reset is irreversible and should be used carefully.

4. **Additional Resource:**
   - For more insights on choosing the right type of reset, refer to this article: [Types of Git Reset](https://archive.is/o/dmkAo/https://medium.com/a-layman/the-learning-note-for-git-version-control-3a4b4f8ab4fc).

# Basic Terminal
To perform a reset in the terminal:

1. Navigate to your Git repository.
2. Use the `git reset` command with the appropriate flag:
   - Soft Reset:
     ```bash
     git reset --soft HEAD~N
     ```
   - Mixed Reset:
     ```bash
     git reset --mixed HEAD~N
     ```
   - Hard Reset:
     ```bash
     git reset --hard HEAD~N
     ```
   Replace `N` with the number of commits to reset.

Understanding these reset options allows you to effectively manage your Git repository's history, whether you're using Lazygit or the terminal.
