---
tags:
  - panel/5
---
# Introduction
This tutorial guides you through the process of deleting a stash in Lazygit. This action is useful when you want to clean up your stash list by removing entries that are no longer needed.

# Lazygit
1. Open Lazygit and navigate to the [[5. Stash]] panel.
2. Use the `↓`/`↑` keys to browse through your stash entries.
3. Select the stash entry you want to delete.
4. Press the `d` key to initiate the deletion of the selected stash.
5. A confirmation prompt will appear. Press `enter` to confirm the deletion.

   - [ ] Add #screenshot showing the stash selection and deletion confirmation prompt.

6. Upon confirmation, the selected stash will be permanently deleted from the stash list.

   - [ ] Add #screenshot of the stash list after deletion.

# Basic Terminal
To delete a stash entry in the terminal:

1. List your stashes to find the one you want to delete:
   ```bash
   git stash list
   ```

2. Delete the specific stash (replace `stash@{n}` with the correct stash identifier):
   ```bash
   git stash drop stash@{n}
   ```

3. Verify the deletion:
   - Run `git stash list` again to ensure the stash has been removed.

This terminal method offers a direct way to manage your stash entries, complementing the Lazygit approach.
