---
title: Point Your Branch Head at Any Arbitrary Commit
tags:
  - fix/audit
---
# Introduction
Performing a hard reset in Git allows you to point the HEAD of your branch to any arbitrary commit. This process is particularly useful when you need to discard changes and align your current branch with a specific state of the repository.

# Basic Terminal
1. **Identify the Commit:**
   - First, determine the commit hash you want to reset to. You can find this by browsing the commit history.
   ```bash
   git log
   ```
   - Look for the hash of the commit you want to reset to.

2. **Performing the Hard Reset:**
   - Use the `git reset` command with the `--hard` option followed by the commit hash.
   ```bash
   git reset --hard <commit-hash>
   ```
   - Replace `<commit-hash>` with the actual hash of the commit you're resetting to.

3. **Effects of Hard Reset:**
   - This command will reset the current branch's HEAD to the specified commit.
   - It will discard all changes in the working directory and index (staging area) since that commit.
   - This action is irreversible, so it's crucial to be certain before performing a hard reset.

# Lazygit
In Lazygit, you can also perform a hard reset:

1. **Open Lazygit and Navigate to Commits:**
   - Launch Lazygit and navigate to the commits panel.

2. **Select the Commit:**
   - Scroll through the list of commits and select the one you want to reset to.

3. **Perform the Hard Reset:**
   - Press the appropriate key (usually `g`) to open the reset options and choose `hard`.
   - Confirm the action if prompted.

   - [ ] Add #screenshot of selecting a commit and performing a hard reset in Lazygit.

Remember, hard reset is a powerful and irreversible operation. It should be used with caution, especially when working in a shared repository.
