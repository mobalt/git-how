---
tags:
  - panel/3
---
# Introduction
This is a guide on how to merge a branch called **"featureA"** into **"main"** branch.


# Lazygit
1. Press `3`  to go to [[3. Local Branches]] panel
2. Press `↓`/`↑` (or `single click`) to hover over **"main"** branch
3. Press `space` (or `double click`) to checkout **"main"** branch
4. Press `↓`/`↑` (or `single click`) to hover over **"featureA"** branch
5. Press `Shift+M` to merge **"featureA"** into **"main"** branch
6. Upon confirmation prompt, press `enter` to continue or `esc` to cancel
    - [ ] Add #screenshot of merge confirmation prompt
7. Resolve any [[merge conflicts]], if any.

# Basic Terminal
1. First checkout the base branch, in this case **main**
```bash
git checkout main
```
2. Merge **"featureA"** into **"main"** branch
```bash
git merge featureA
```
3. If there are merge conflicts, you will need to resolve them before you can complete the merge.
```bash
# To select changes done in base `main` branch
git checkout --ours <file>

# To select changes done in `featureA` branch
git checkout --theirs <file>

# or Manually edit the file to resolve the conflict
vim <file>
```
4. Once conflicts are resolved for a file, stage the file
```bash
git add <file>
```
5. Once all conflicts are resolved, complete the merge
```bash
git merge --continue
```
