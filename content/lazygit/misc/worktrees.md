---
tags:
  - panel
---
# Introduction
Git worktrees are an advanced feature that allows you to work with multiple branches in separate working directories. This guide will explain how to manage worktrees using Lazygit and provide an overview of using worktrees in the basic terminal.

# Lazygit
1. **Navigating to Branches View:**
   - Open Lazygit and navigate to the branches view. This can typically be accessed by pressing a designated key (often `2` or `3` depending on your layout).

2. **Creating a Worktree:**
   - Select the branch you want to create a worktree from.
   - Press `w` to create a new worktree for the selected branch. Lazygit will handle the creation and checkout process automatically.

3. **Switching to the Worktree:**
   - Lazygit will switch to the new worktree directory, allowing you to work on this branch in a separate directory from your main repository.

   ![Creating Worktree in Lazygit](991fb6c210af82f9f3b49f5286a355de_MD5.gif)

# Basic Terminal
1. **Creating a Worktree:**
   - In your terminal, navigate to your Git repository.
   - Use the `git worktree` command to create a new worktree:
     ```bash
     git worktree add <path-to-new-worktree> <branch-name>
     ```
   - Replace `<path-to-new-worktree>` with the directory path for the new worktree and `<branch-name>` with the branch you want to check out.

2. **Navigating to the Worktree:**
   - Change directory to the path you specified for the new worktree.
   - You can now work on this branch independently of your main repository.

3. **Removing a Worktree:**
   - When you're done with a worktree, remove it to clean up:
     ```bash
     git worktree remove <path-to-worktree>
     ```

4. **Listing Worktrees:**
   - To see all active worktrees, use:
     ```bash
     git worktree list
     ```

# Conclusion
Worktrees are a powerful feature in Git that provide the flexibility to work on multiple branches simultaneously without affecting the main repository. Lazygit simplifies the process of managing worktrees, making it more accessible, while command-line alternatives offer more control for those comfortable with terminal operations.
