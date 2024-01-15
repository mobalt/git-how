---
title: Commit staged files
tags:
  - panel/2
---
# Lazygit
1. You need to stage some content first, using one of these methods
    - [[all files|Stage: All Changed Files]]
    - [[entire file|Stage: Entire File]]
	- [[specific lines|Stage: Specific Lines]]
2. Press `2` to go to [[2. Files]]
3. Press one of these keys:
    - `c` to commit the staged changes
    - `C` to commit with $EDITOR
    - `w` to commit without running pre-commit hooks
4. Enter the commit message.
    - The 80-char subject goes on the first line. Describes what the commit does.
    - The longer body goes on the second line. Describes intention behind the commit. Why?
    - Press `tab` to move between the subject and body.
4. Press `enter` to commit.
5. The commit should now be visible in the [[4. Commits]] panel.
    - Note it is a different color than existing commits, to signify that this commit is local and has not yet been pushed to remote.

# Basic Terminal
Add message inline
```bash
git commit -m "commit message"
```

Or to open your default `$EDITOR`:
```bash
git commit
```
