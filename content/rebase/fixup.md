---
tags:
  - panel/4
  - fix/audit
aliases:
  - Delete the old commit message, only keep new merged commit
---
# Introduction
In Git, "fixup" is a technique used to merge changes from one commit into a previous one, while discarding the commit message of the merged commit. This is useful for cleaning up a series of commits before sharing them publicly. This tutorial will guide you through the process of using the fixup command in Lazygit.

# Lazygit
Using fixup in Lazygit simplifies the process of combining commits without retaining unnecessary commit messages. Here’s how you can do it:

1. **Select the Commit:**
   - Open Lazygit in your repository.
   - Navigate to the **Commits** panel by pressing `1`.
   - Use the arrow keys to hover over the commit that you want to merge into another commit (the "later commit").

2. **Apply Fixup:**
   - Once you have selected the later commit, press `f` to perform a fixup.
   - This action will squash the selected commit into the specified target commit (generally the commit just before it) and discard the commit message of the fixup commit.
   - The changes from the fixup commit are kept, but the commit message is not.

3. **Finalize Changes:**
   - Lazygit will automatically handle the rebase and fixup process.
   - Once completed, the history will be rewritten to reflect the combined changes of the original and fixup commits, with only the original commit message retained.

# Basic Terminal
To perform a fixup in the terminal:

1. Start an interactive rebase:
   ```bash
   git rebase -i <commit-hash>^
   ```
   Replace `<commit-hash>` with the hash of the commit just before the one you want to squash.

2. In the interactive rebase todo list, change `pick` to `fixup` for the commit you want to combine.

3. Save and exit the editor, and Git will automatically apply the fixup.

4. If there are any conflicts, resolve them and then continue the rebase:
   ```bash
   git rebase --continue
   ```

# Conclusion
The fixup command in Lazygit is a convenient tool for cleaning up your commit history by merging changes while discarding specific commit messages. It's particularly useful for combining small fixes or amendments into a single cohesive commit. The terminal alternative requires a few more steps but offers the same functionality. Remember, rewriting history with commands like fixup should be done cautiously, especially in shared repositories.
