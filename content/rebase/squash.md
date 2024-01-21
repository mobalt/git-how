---
tags:
  - panel/4
  - fix/audit
aliases:
  - Append old commit message, to new merged commit
---
# Introduction
Squashing commits in Git is a way of combining multiple commit changes into a single commit. This is particularly useful for cleaning up your commit history, merging small fixes, or consolidating changes made over several commits into a more coherent package. This tutorial will guide you through squashing commits using Lazygit.

# Lazygit
Here's how to squash commits in Lazygit:

1. **Select the Commit to Squash:**
   - Open Lazygit in your repository.
   - Navigate to the **Commits** panel by pressing `1`.
   - Hover over the later commit that you want to squash into a prior commit. This is typically a more recent commit that you want to combine with an older one.

2. **Squash the Commit:**
   - With the commit selected, press `s` to squash it down. This action combines the selected commit with the one directly below it.
   - A dialog box may appear asking you to edit the commit message for the new, squashed commit. This is where you can combine the messages from the squashed commits or write a new one.

3. **Finalize the Squash:**
   - Complete the squash operation. Lazygit will automatically handle the rebase process to rewrite the commit history.
   - Once completed, the changes from the squashed commit will be merged into the previous commit, and the commit history will be updated.

# Basic Terminal
To squash commits using the terminal:

1. Start an interactive rebase:
   ```bash
   git rebase -i HEAD~<number>
   ```
   Replace `<number>` with the count of commits you want to include in the rebase.

2. In the interactive rebase list, mark the commit you want to squash with `squash` or `s` next to it.

3. Save and close the editor. Git will then prompt you to merge the commit messages.

4. After adjusting the commit message, continue the rebase:
   ```bash
   git rebase --continue
   ```

# Conclusion
Squashing commits in Lazygit simplifies the process of combining multiple commits into one, making your project history cleaner and more understandable. The terminal method is a more manual approach but provides greater control over the squashing process. Remember, squashing rewrites your project's history, so it should be done with caution, especially when working with shared branches or after pushing to remote repositories.
