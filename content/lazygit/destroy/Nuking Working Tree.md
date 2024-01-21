---
tags:
  - panel/2
  - fix/audit
---
# Introduction
"Nuking" the working tree in Git is a term used to describe the action of removing all untracked files and resetting any changes made to tracked files in your working directory. This guide will explain how to perform this action in Lazygit.

# Lazygit
1. **Accessing the Files Panel:**
   - Press `2` to navigate to the [[2. Files]] panel. This panel shows all the changed files in your repository.

2. **Nuking the Working Tree:**
   - Once in the Files panel, use `↓`/`↑` keys or a `single click` to highlight any file (this is just to focus the panel).
   - Press `Shift+D` to bring up the reset options menu.

3. **Selecting the 'Nuke' Option:**
   - In the menu that appears, select the 'nuke' option.
   - This action will remove all untracked files (those not tracked by Git) and revert any modifications made to tracked files since the last commit.

   ![Reset Options Menu](Pasted image 20230722120429.png)

4. **Effect of Nuking:**
   - This is equivalent to cleaning your working directory to its state as per the last commit, effectively removing anything that would show up in `git status`.
   - It's a drastic action and should be used with caution as it will irreversibly remove untracked files and changes.

![Nuking Working Tree Demo](170510441fd1ddec1dfe4e543f727f1b_MD5.gif)

# Use Case
- **When to Use This Feature:**
  - 'Nuking' is useful when you want to start fresh without any uncommitted changes or untracked files cluttering your working directory.
  - It's particularly handy in scenarios where you have a lot of generated or temporary files that are not part of the repository, and you want to quickly clean up.

# Conclusion
Understanding how to 'nuke' your working tree in Lazygit can be a powerful tool for maintaining a clean and manageable Git workspace. However, given its irreversible nature, it should be used judiciously.
