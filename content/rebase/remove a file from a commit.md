---
tags:
  - panel/4
---
### Deleting a Change

# Introduction
Sometimes, you might find yourself needing to remove an entire file's changes from a specific commit in your Git history. This could be due to various reasons, such as accidentally committing sensitive data or simply including changes that should not have been part of that commit. Lazygit provides a straightforward way to handle this scenario.

# Lazygit
Here's how to delete the entire changes of a file from a commit using Lazygit:

1. **Navigate to the Commit:**
   - Open Lazygit and go to the **Commits** panel.
   - Find the commit that contains the file whose changes you want to delete.

2. **Select the File:**
   - Press `enter` on the commit to view the list of files affected by that commit.
   - Navigate to and highlight the file you want to modify.

3. **Delete the Changes:**
   - With the file selected, press `d` to delete all changes made to that file in the selected commit.
   - A confirmation dialog will appear, asking you to confirm the deletion of changes. This step ensures that you are aware of the rebase that will take place to remove these changes.

4. **Confirm and Complete:**
   - Confirm the deletion. Lazygit will perform an interactive rebase to remove the changes from that particular file in the specified commit.

### Basic Terminal
To remove a file's changes from a commit using the terminal:

1. Start an interactive rebase:
   ```bash
   git rebase -i <commit-hash>^
   ```
   Replace `<commit-hash>` with the hash of the commit just before the one you want to edit.

2. Mark the commit with `edit`.

3. When the rebase stops at the commit, remove the file's changes:
   ```bash
   git reset HEAD^ <file>
   git commit --amend
   ```

4. Continue the rebase process:
   ```bash
   git rebase --continue
   ```

# Conclusion
Deleting a file's changes from a commit is a useful way to correct mistakes in your Git history. Lazygit streamlines this process with its intuitive interface, making it accessible even for those less familiar with Git's complexities. The terminal method offers a more manual approach but requires a good understanding of Git commands and interactive rebase. It's important to use these techniques carefully, especially when working with shared branches or remote repositories.
