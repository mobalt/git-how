---
tags:
  - panel/4
---
# Introduction
Cherry-picking commits in Git allows you to selectively copy individual commits from one branch into another. This is particularly useful when you want to apply specific changes without merging all the changes from another branch. Lazygit simplifies this process with a user-friendly "copy-and-paste" model.

# Lazygit
Follow these steps to cherry-pick commits in Lazygit:

1. **Select Source Commit:**
   - Open Lazygit in your repository.
   - Navigate to the **Branches** panel by pressing `2`.
   - Scroll to the source branch (the one containing the commit(s) you wish to cherry-pick) and press `enter` to switch to the commits panel.
   - Scroll to the desired commit(s) and press `c` to copy each commit you want to cherry-pick. Copied commits will be highlighted, as shown in the image ![[Pasted image 20230722115941.png]].

2. **Switch to Target Branch:**
   - Press `esc` to return to the **Branches** panel.
   - Ensure the target branch (the one you want to cherry-pick the commits into) is checked out. It should have a `*` next to it. If it's not checked out, use `space` to select and check it out.

3. **Paste Commits:**
   - Navigate to the **Commits** panel by pressing `1`.
   - Press `v` to paste the cherry-picked commits onto the target branch. The cherry-pick action will be applied, as demonstrated in the image ![[Pasted image 20230722120059.png]].

# Basic Terminal
To perform cherry-picking in the terminal:

1. Check out the target branch:
   ```bash
   git checkout <target-branch>
   ```

2. Cherry-pick individual commit(s) from the source branch:
   ```bash
   git cherry-pick <commit-hash>
   ```
   Repeat this command for each commit you wish to cherry-pick.

3. Resolve any conflicts that arise during the cherry-pick process, and then finalize the cherry-pick:
   ```bash
   git cherry-pick --continue
   ```

# Conclusion
Cherry-picking is a powerful feature in Git for selectively applying changes from one branch to another. Lazygit's intuitive interface makes this process more accessible, especially for beginners. The basic terminal commands offer an alternative method for more experienced users. Remember, cherry-picking should be used judiciously to maintain a clean and understandable history in your repository.
