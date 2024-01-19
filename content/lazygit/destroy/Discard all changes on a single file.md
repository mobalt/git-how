---
tags:
  - panel/2
---
# Introduction
Discarding changes in a specific file is a common requirement in version control management. This tutorial will guide you through discarding changes in a single file using Lazygit, a simple yet powerful Git interface.

# Lazygit
1. **Navigate to Files Panel:**
   - Press `2` to go to the [[2. Files]] panel in Lazygit.
   - Here, you'll see a list of changed files in your repository.

2. **Selecting the File:**
   - Use `↓`/`↑` keys or a `single click` to hover over the file whose changes you want to discard.

3. **Discard Changes in a File:**
   - Once the desired file is highlighted, press `d` to discard changes in that file.
   - This action will not delete the file but will revert any modifications made to it since the last commit.

   ![Discarding Changes](Pasted image 20230722120236.png)

### Understanding Different Options
- **`D` vs `d`:**
  - `d` is for discarding changes in the selected file.
  - `D` (uppercase) opens a menu with options to clean or reset the working tree, which are less frequently used but offer more control over discarding changes.

- **`g` for Resetting from Upstream:**
  - Pressing `g` in the files section lets you reset your tree to a remote tracking branch. This offers options for soft, hard, or mixed resets to the upstream branch.
  - It's particularly useful when you need to align your work with a version of the branch that has been updated remotely, like after a force push.

![Discarding Changes Menu](files-nuke.png)
![Reset from Upstream](reset-upstream.png)

# Conclusion
Lazygit provides various options for discarding changes, from simple file-specific changes to more complex repository-wide resets. Understanding these options allows you to manage your Git repository efficiently and effectively.
