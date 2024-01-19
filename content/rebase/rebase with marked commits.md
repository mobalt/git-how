---
tags:
  - panel/4
  - fix/plagiarize
---

### Rebase from Marked Base Commit

# Introduction
Rebasing from a specific base commit is a powerful Git technique used when you need to change the base of your feature branch. For example, if your feature branch is based on `develop`, but you need it to be based on `master`, Lazygit provides a straightforward way to achieve this with the ability to mark a base commit and rebase onto a different branch.

# Lazygit
Here's how to rebase from a marked base commit in Lazygit:

1. **Identify and Mark the Base Commit:**
   - Open Lazygit and navigate to the **Commits** panel of your feature branch.
   - Identify the last commit on the original base branch (e.g., `develop`).
   - Press `Shift + B` to mark that commit as your base commit. This commit acts as a boundary: only commits above it (more recent ones) will be included in the rebase.

2. **Perform the Rebase:**
   - Navigate to the **Branches** panel and select the branch you want to rebase onto (e.g., `master`).
   - Press `r` to start the rebase process. This will rebase your feature branch onto the selected branch, including only the commits after your marked base commit.

3. **Push Changes:**
   - After successfully rebasing, you can push your changes to the remote repository by pressing `Shift + P`.

4. **Visual Demonstration:**
   - For a visual guide on how this works, check out the demonstration gif from Lazygit: [Rebase Onto Demo](https://github.com/jesseduffield/lazygit/blob/assets/demo/rebase_onto-compressed.gif).

### Rebasing onto Another Branch (v0.40+)

In Lazygit release 0.40, `rebase --onto` support was introduced, enhancing the rebasing process:

- To select a base commit for rebasing, choose it in the commits panel and press `Shift + B`.
- The panel will visually change, showing arrows on the first commit not included in the rebase, clarifying which commits will be rebased.
- Proceed to rebase from the branches panel as usual.

![[rebase-onto.png]]

# Basic Terminal
To perform a similar rebase in the terminal:

1. Start the rebase process:
   ```bash
   git rebase --onto <new-base> <old-base>
   ```
   Replace `<new-base>` with the branch you want to rebase onto (e.g., `master`) and `<old-base>` with the commit just before the first commit of your feature branch.

2. Resolve any conflicts that arise during the rebase.

3. Continue the rebase process:
   ```bash
   git rebase --continue
   ```

4. Force push your changes if the branch was previously pushed:
   ```bash
   git push --force-with-lease
   ```

# Conclusion
Rebasing from a marked base commit in Lazygit simplifies the process of changing the base of your feature branch, making it more intuitive and less error-prone. The terminal commands provide a more manual but equally effective way to achieve the same result. Be cautious with rebasing, especially when working with branches that are shared or already pushed to remote repositories.
