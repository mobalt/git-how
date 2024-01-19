---
tags:
  - panel/2
---
# Introduction
Reverting uncommitted changes in Git is a common task, useful for undoing recent modifications that you don't want to keep. This guide will help you understand how to revert these changes using both Lazygit and Git commands.

# Lazygit
1. **Accessing the Files Panel:**
   - Press `2` to open the [[2. Files]] panel in Lazygit. This displays a list of files with uncommitted changes.

2. **Selecting the File:**
   - Use `↓`/`↑` keys or a `single click` to hover over the file you want to revert changes for.

3. **Reverting Changes:**
   - Press `D` (uppercase) to open a menu with options for reverting changes.
   - Within this menu, press `u` to discard unstaged changes in the selected file.

   ![Lazygit Reversions](lazygit_reversions.webp)

# Git Commands for Reverting Changes
1. **Nuke Working Tree:**
   - To discard all changes (staged, unstaged, and untracked):
     ```bash
     git reset --hard HEAD && git clean -fd
     ```
   - This command resets your working tree to the last commit and removes untracked files and directories.

2. **Discard Unstaged Changes:**
   - To revert changes that are not staged for commit:
     ```bash
     git checkout -- .
     ```

3. **Discard Untracked Files:**
   - To remove untracked files from your working directory:
     ```bash
     git clean -fd
     ```

4. **Discard Staged Changes:**
   - To undo changes that have been staged (but not committed):
     ```bash
     # Stash staged changes and drop the stash
     git stash --keep-index
     git stash drop
     ```

5. **Reset Types:**
   - **Soft Reset:** Keeps all changes in your working directory.
     ```bash
     git reset --soft HEAD
     ```
   - **Mixed Reset:** Unstages changes, but keeps them in your working directory.
     ```bash
     git reset --mixed HEAD
     ```
   - **Hard Reset:** Discards all changes since the last commit.
     ```bash
     git reset --hard HEAD
     ```

# Conclusion
Understanding how to revert changes in Lazygit and using Git commands provides flexibility in managing your repository. Whether you need to discard a few unstaged changes or reset your entire working tree, these tools offer effective solutions.
