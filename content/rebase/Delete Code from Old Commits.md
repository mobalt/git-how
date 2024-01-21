---
tags:
  - panel/4
  - fix/audit
---
# Introduction
Modifying old commits to delete specific changes can be a tricky task in Git, especially when those changes impact subsequent commits. This tutorial will guide you through the process of removing a change from an old commit using Lazygit's patch functionality, which essentially performs an interactive rebase under the hood.

# Lazygit
Here's how to delete code from old commits using Lazygit:

1. **Select the Commit:**
   - Open Lazygit in your repository.
   - Navigate to the **Commits** panel by pressing `1`.
   - Scroll to find the commit from which you want to remove a specific change.

2. **Create a Custom Patch:**
   - Once you've selected the commit, press `Ctrl + P` to access the **Patch Options** menu.
   - In the Patch Options, choose "**remove patch from original commit**". This action creates a custom patch that excludes the specific changes you want to remove.

3. **Handle Merge Conflicts:**
   - If your change ("cola" in this case) is altered in later commits (like being swapped for "lemonade"), you might encounter a merge conflict.
   - Lazygit will display a conflict notification, as shown in the image ![[Pasted image 20230722135846.png]].
   - Press `enter` to start resolving the conflict. You can resolve conflicts within Lazygit or use your preferred text editor.

4. **Complete the Interactive Rebase:**
   - After resolving the conflict, Lazygit will automatically continue the interactive rebase process.
   - Ensure that the rebase completes successfully and that the unwanted change is removed from the original commit.

# Basic Terminal
To achieve a similar result in the terminal:

1. Start an interactive rebase for the commits in question:
   ```bash
   git rebase -i <commit-hash>^
   ```
   Replace `<commit-hash>` with the hash of the commit just before the one you want to edit.

2. Mark the commit you want to edit with `edit` instead of `pick`.

3. When Git pauses at that commit, make the necessary changes to your code.

4. Stage your changes and amend the commit:
   ```bash
   git add .
   git commit --amend
   ```

5. Continue the rebase process:
   ```bash
   git rebase --continue
   ```

6. Resolve any merge conflicts that arise, and complete the rebase.

# Conclusion
Editing old commits to remove specific changes is a complex operation but can be efficiently handled with Lazygit's patch and interactive rebase features. The terminal method offers a more manual approach but provides the same level of control. Be cautious when editing historical commits, as it can change your project's history. This action should be avoided on shared branches or after the changes have been pushed to a remote repository.
