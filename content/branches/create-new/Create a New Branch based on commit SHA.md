---
tags:
  - panel/4
---
# Lazygit
1. Press `3`, to go to [[3. Branches]]
2. Select the branch that contains the commit-of-interest
    - Using `↓`/`↑` (or `single click`)
3. Press `enter`, to go drill-down into the branch, and see its commits
4. Select the commit-of-interest, using `↓`/`↑` (or `single click`)
5. Press `n`, to create a new branch
6. Enter branch name into pop-up menu, below:
    - [ ] Add #screenshot of pop-up menu for entering branch name off of commit
5. Press `enter`, to continue.
6. You should now see your new branch created and checked out (with `*` star)
    - [ ] Add #screenshot of new branch with star

# Basic Terminal
1. Find the commit SHA of the commit-of-interest
```bash
git log --oneline --graph
```
2. Copy the commit SHA
3. Paste the commit SHA into the following command
```bash
git checkout -b <new-branch-name> <commit-SHA>
```
