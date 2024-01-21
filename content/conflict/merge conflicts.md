---
tags:
  - fix/audit
---
# Introduction
Merge conflicts in Git occur when two branches have made edits to the same part of a file and Git is unable to automatically resolve these changes. Understanding how to address these conflicts is essential for smooth collaboration and maintaining a clean project history.

# Context
## Scenario 1: Merge
When merging branches (e.g., merging `featureA` into `main`), conflicts may arise:
1. Switch to the main branch:
   ```bash
   git checkout main
   ```
2. Merge the feature branch:
   ```bash
   git merge featureA
   ```

## Scenario 2: Rebase
Conflicts can also occur during rebase operations:
1. Rebase a feature branch onto the main branch:
   ```bash
   git rebase main featureA
   ```

## Conflict Example
Conflicts are indicated in the file with markers:
```
<<<<<<<< HEAD
if x == 0:
  return false
========
if y == 6:
  return true
elif x == 0:
  return false
>>>>>>> d123456
```

# Resolving the Conflict
## Manually
1. Open the file in a text editor:
   ```bash
   vim conflict_file.txt
   ```
2. Resolve the conflict by choosing one of the options:
   - **Option 1:** Keep "OUR" change (current branch)
   - **Option 2:** Keep "THEIR" change (other branch)
   - **Option 3:** Write a new resolution

## Using GUI
1. Run `git mergetool` for a GUI-based conflict resolution tool like Meld.

## Using vim's Fugitive
- [ ] Write how to resolve merge conflicts using Fugitive.

## Using Lazygit
- [ ] Write how to resolve merge conflicts using Lazygit.

# Continuing After Resolution
1. Stage the resolved files:
   ```bash
   git add <resolved-files>
   ```
2. Check for remaining conflicts:
   ```bash
   git diff --check
   ```
3. Continue the merge or rebase:
   - For merge:
     ```bash
     git merge --continue
     ```
   - For rebase:
     ```bash
     git rebase --continue
     ```

# Additional Notes
- The `--ours` and `--theirs` options can be used in both `merge` and `rebase` scenarios to choose changes from the current branch or the incoming branch, respectively.
- Always ensure conflicts are fully resolved and the code is functional before continuing with merges or rebases.

Understanding and resolving merge conflicts is a critical skill in Git, enabling smoother integration of changes from different branches.
