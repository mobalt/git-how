# Basic Terminal
## Last Commit
1. Be familiar with [[Preparing to Modify History]]
2. Undo your last commit:
```bash
git reset HEAD~
# is equivalent to
git reset HEAD~ --mixed
# which clears the commit, the stage, but leaves the working directory alone
```
3. Stage the changes you want for your first commit
```bash
git add <file1> <file2> <file3>
# or
git add -p <file1> # to stage specific lines
```
4. Commit your first commit
```bash
git commit -m "First commit"
# or
git commit # to open your default $EDITOR
```
5. Repeat steps 3 and 4 for your second commit, and any additional commits you want to make.
6. Make sure there are no uncommitted changes left in your working directory
```bash
git status # should be empty of changes
```
7. If you stashed changes, you can get them back
```bash
git stash pop
```

## Deeper Commit
1. Be familiar with [[Preparing to Modify History]]
2. Copy the SHA of the commit you want to split
```bash
git log --oneline --graph
```
3. Do an interactive rebase, starting from the commit before the one you want to split
```bash
git rebase -i <commit-before-the-one-you-want-to-split>
# or
git rebase -i <commit-you-want-to-split>~
# or
git rebase -i <commit-you-want-to-split>^
```
4. This will open your default $EDITOR with a list of commits, and the default rebase action for each commit is `pick`
```
pick 9f8f3f0 Commit 1
pick 3f8f3f0 Commit 2
pick 1f8f3f0 Commit you want to Split
```
5. Change the action for the commit you want to split to `edit`
```
pick 9f8f3f0 Commit 1
pick 3f8f3f0 Commit 2
edit 1f8f3f0 Commit you want to Split
```
6. Save and close the file. This will rewind your working directory to just after the commit you want to split.
7. Undo the commit you want to split
```bash
git reset HEAD~
```
8. Stage the changes you want for your first commit
```bash
git add <file1> <file2> <file3>
# or
git add -p <file1> # to stage specific lines
```
9. Commit your first commit
```bash
git commit -m "First commit"
# or
git commit # to open your default $EDITOR
```
10. Repeat steps 3 and 4 for your second commit, and any additional commits you want to make.
11. Make sure there are no uncommitted changes left in your working directory
```bash
git status # should be empty of changes
```
12. Now you'll want the interactive rebase to finish by replaying the rest of the commits
```bash
git rebase --continue
```
13. If you stashed changes, you can get them back
```bash
git stash pop
```
