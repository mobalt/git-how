---
tags:
  - panel/2
  - fix/audit
---
# Introduction
This guide demonstrates how to add files to a stash using Lazygit. Stashing is useful for temporarily setting aside changes in your working directory.

# Lazygit
1. Press `2` to switch to the [[2. Files]] panel.
2. Navigate to the desired files using `↓`/`↑` keys or a `single click`.
3. Once you've highlighted a file:
   - Press the `s` key to mark individual files for stashing.
4. Observe the changes in the **Files** window as you select files for stashing.

   ![Files Window with Selected Files](01427bd1e49c7c5d0a948099d0ce9365_MD5.webp)

5. For regular stashing, press `s`. However, for more options:
   - Press `Shift+S` to access the **Stash Options** menu.

   ![Stash Options Menu](Pasted image 20230722132623.png)

6. In the **Stash Options** menu:
   - Choose **"stash staged changes"** and press `Enter`.
   - Enter a message for your stash when prompted.

   ![Enter Stash Message](Pasted image 20230722132743.png)

7. Confirm the stash is created:
   - Look at the bottom-left window to see your new stash entry.

   ![Stash Entry Confirmation](Pasted image 20230722132815.png)

# Basic Terminal
To perform a similar action in the terminal:

1. Stage the files you want to stash:
   ```bash
   git add <file1> <file2> ...
   ```

2. Stash the staged changes with a message:
   ```bash
   git stash push -m "Your stash message"
   ```

3. To confirm the stash was created:
   ```bash
   git stash list
   ```

This process in the terminal provides a straightforward way to handle stashing, complementing the Lazygit approach.
