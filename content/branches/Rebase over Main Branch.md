---
tags:
  - panel/3
---
# Introduction
This is a guide on how to rebase a branch called **"feature"** over **"main"** branch.

# Lazygit
1. Press `3`  to go to [[3. Local Branches]] panel.
2. Select the **feature** branch (using `↓`/`↑`/🖱️).
3. Check out the **feature** branch (press `space`).
4. Select the **main** branch (using `↓`/`↑`/🖱️).
5. Press `r` to rebase the **feature** branch over **main** branch.
6. Press `enter` to continue.
    - [ ] Add #screenshot of rebase confirmation prompt.
7. Resolve any [[merge conflicts]], if any.
    - [ ] Add #screenshot of **Auto-merge failed** notification

# Basic Terminal
1. First checkout the feature branch that you want to rebase
```bash
git checkout feature
```
2. Then rebase it over **main** branch
```bash
git rebase main
```
3. If there are conflicts, you will need to resolve them before you can continue the rebase.
```bash
# To select changes done in base `main` branch
git checkout --ours <file>

# To select changes done in `feature` branch
git checkout --theirs <file>

# or Manually edit the file to resolve the conflict
vim <file>
```

4. Once conflicts are resolved for a file, stage the file
```bash
git add <file>
```

5. Once all conflicts are resolved, continue the rebase
```bash
git rebase --continue
```

# See Also
- [[Resolving Merge Conflicts]]
