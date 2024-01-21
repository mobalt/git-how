---
tags:
  - panel/5
  - fix/audit
---
# Introduction
This guide explains how to apply files from a stash in Lazygit without removing the stash entry. This method is useful for reapplying changes from a stash while keeping the stash intact for future use.

# Lazygit
1. Open Lazygit and navigate to the [[5. Stash]] panel.
2. Use the `↓`/`↑` keys to select the stash entry you want to apply.
3. Once the desired stash is selected, press the `spacebar` to apply the changes from the stash to your working directory.
4. After pressing `spacebar`, the changes in the selected stash will be applied, but the stash entry itself will remain in the stash list.

   - [ ] Add #screenshot showing the selected stash and the action of applying it.

5. Verify the changes:
   - Check your working directory to ensure that the changes from the stash have been correctly applied.

   - [ ] Add #screenshot of the working directory after applying stash.

# Basic Terminal
To achieve the same in the basic terminal:

1. List available stashes to find the one you want to apply:
   ```bash
   git stash list
   ```

2. Apply the stash without removing it from the stash list (replace `stash@{n}` with the correct stash identifier):
   ```bash
   git stash apply stash@{n}
   ```

3. Check your working directory to confirm the changes:
   - Use `git status` or manually inspect the files to ensure the stash's changes are present.

This method provides a straightforward way to reapply stashed changes while retaining the stash for potential future use.
