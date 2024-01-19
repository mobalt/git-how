---
tags:
  - panel/5
---
# Introduction
This guide focuses on how to pop files from a stash using Lazygit. Popping a stash applies the changes in the stash to your workspace and, if there are no merge conflicts, automatically deletes the stash entry. This is a common operation when you want to reintegrate stashed changes and clean up the stash list.

# Lazygit
1. Open Lazygit and navigate to the [[5. Stash]] panel.
2. Use the `↓`/`↑` keys to select the stash entry you wish to pop.
3. Once the desired stash is selected, press the `g` key to pop the stash.
4. When you press `g`, Lazygit will attempt to apply the stashed changes to your workspace. If there are no merge conflicts, the stash entry will be automatically removed from the list.

   - [ ] Add #screenshot showing the selected stash and the pop action.

5. Check for merge conflicts:
   - If merge conflicts arise, you will need to resolve them manually. After resolving, the stash will still need to be manually deleted.
   - If there are no conflicts, the stash entry will be removed, and the changes will be applied to your workspace.

   - [ ] Add #screenshot of the workspace after popping the stash, indicating the status of merge conflicts if any.

# Basic Terminal
To pop a stash in the terminal:

1. List the stashes to find the one you want to pop:
   ```bash
   git stash list
   ```

2. Pop the selected stash (replace `stash@{n}` with the correct identifier):
   ```bash
   git stash pop stash@{n}
   ```

3. Resolve any merge conflicts if they arise. After resolving them, the stash entry will automatically be removed if there are no conflicts.

This terminal method complements the Lazygit approach and provides a straightforward way to manage and apply stashed changes.
