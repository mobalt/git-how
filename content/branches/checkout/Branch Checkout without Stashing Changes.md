---
tags:
  - panel/3
  - fix/audit
---
# Introduction
This tutorial will guide you through the process of checking out a different branch in Git without losing your current changes. This is particularly useful when you need to switch branches but have uncommitted changes that you're not ready to commit.

# Lazygit
Lazygit offers a straightforward way to handle this situation through its autostash feature. Here's how to use it:

1. Open Lazygit in your repository.
2. Navigate to the **Branches** panel by pressing `2`.
3. Use the `↓`/`↑` keys or your mouse to select the branch you want to switch to.
4. Press `enter` to attempt to check out the new branch.
5. You will encounter an **Autostash** message, as shown in the image ![[Pasted image 20230722141828.png]]. This message indicates that Lazygit can temporarily stash your changes, check out the new branch, and then reapply your changes.
6. Press `enter` to confirm and proceed with the autostashing process. Lazygit will handle the stashing and reapplying of your changes automatically.
7. Once the checkout is complete, ensure that your changes are reapplied correctly. In some cases, you might need to resolve merge conflicts if the changes in the stashed files conflict with the new branch.

   - **Tip:** If you encounter conflicts, Lazygit will alert you. You can resolve these conflicts within Lazygit or use your preferred text editor.

8. After resolving any conflicts, continue working on your newly checked out branch.

# Basic Terminal
If you prefer to use the terminal, you can achieve a similar result with Git commands:

1. Stash your changes in the current branch:
   ```bash
   git stash
   ```
2. Checkout the branch you want to switch to:
   ```bash
   git checkout <branch-name>
   ```
3. Apply your stashed changes to the new branch:
   ```bash
   git stash pop
   ```

   - **Note:** If there are any conflicts after applying the stash, you'll need to resolve them manually in your preferred text editor.

4. After resolving conflicts, if any, you can continue your work on the new branch.

# Conclusion
Switching branches without losing your current work is a common scenario in Git workflows. Lazygit's autostash feature simplifies this process, making it more efficient and less error-prone, especially for beginners. For terminal users, the traditional `git stash` method is always a reliable alternative.
