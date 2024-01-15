We will go over each of the left panels. Now is a good time to remember that you can press `1-5` to move focus to specific panels.

# 1. Status
The top-left most panel. This panel shows you the git repo you are in, the current branch, and the overall status of your repo.
- `↑` - number of commits ahead of remote
    - mnemonic: How many commits can I push up into the cloud above me?
- `↓` - number of commits behind remote
    - mnemonic: How many commits can I pull down from the cloud above me?

- [ ] #screenshot of panel 1 with commits ahead and behind

Additionally, it has a few cool actions:
- `e` - [[edit lazygit configuration file]]
- `ctrl+r` - [[switch to a recent git repo]]

# 2. Files
This panel is like `git status` in that it shows the modified files in your working directory.

It shows a list of files that have changes which have not yet been commited to the repo.

## Legend
- **color** - indicates the status of the file
    - `red` - unstaged
    - `green` - staged
- Status **code**
    - `?` - untracked
    - 'A' - added
    - 'M' - modified
    - 'D' - deleted

## Use
This panel is useful for staging, unstaging, and committing files. The default action (`spacebar`) will toggle the staged status of the file.

# 3. Local branches
This panel shows you:
- `*` - (topmost line) the currently checked out branch
- the most recent branches
- the status (`↑`/`↓`) relative to the remote branch
- [ ] #screenshot of panel 3 with commits ahead and behind

## Use
This panel is useful for checking out branches. The default action (`spacebar`) will checkout the branch. Panel "4. Commits" will change to show the commits on that branch.

If you want to look at the commits on a branch, without checking it out, you can press `enter` to "drill-down" into the branch.
The panel will change to show you the commits on that branch. If you "drill-down" into a commit, the panel will change to show you the files that were changed in that commit.
- [ ] #screenshot of panel 3 "drill-down"-ed into the commits. Show how this is different from panel 4.

# 4. Commits
This panel shows the commits, for the currently checked out branch, with most recent first.

- [ ] #screenshot of panel 4

# 5. Stash
This panel shows the stash stack, with most recent first.

- [ ] #screenshot of panel 5
