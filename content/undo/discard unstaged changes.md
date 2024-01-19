---
aliases:
  - I need to undo my changes to a file!
sources: osg
---

# Introduction
Sometimes in Git, you may find yourself needing to undo changes made to a specific file, reverting it back to a previous state. This can be done by checking out a previous commit for that file. Below, we'll explore how to revert a single file and also discuss reverting a specific patch or an entire commit.

# Undo Changes to a Single File
## Finding the Right Commit
First, identify the commit you want to revert to. Use `git log` to browse your commit history:

```bash
git log
```

- Scroll through the history using the arrow keys.
- Once you find the desired commit, note down its hash.

## Reverting the File
To revert the file to the version in the saved commit:

```bash
git checkout [saved hash] -- path/to/file
```

- This command replaces your current version of the file with the one from the specified commit.
- The file will now be staged and ready for commit.

## Committing the Reversion
Commit this change to finalize the reversion:

```bash
git commit -m "Reverted file to previous version"
```

## Understanding the Command
The `git checkout` command can be confusing, but it's versatile. In this context, it's used to update a specific file in your working directory to its state at a specific commit.

# How to Revert a Specific Patch or Whole Commit
To revert changes more granularly, such as a specific patch or an entire commit, you can use different strategies:

## Reverting a Patch (`-p` Option)
- You can revert specific changes (patches) in a file:

  ```bash
  git checkout -p <commit-hash> -- <file-path>
  ```

  - The `-p` option allows you to interactively choose which patches to revert.

## Reverting an Entire Commit
- To revert all changes from a specific commit:

  ```bash
  git revert <commit-hash>
  ```

  - This command creates a new commit that undoes all changes introduced by the specified commit.

## Important Note
- **Commit before Reverting**: Before reverting changes, ensure you have no uncommitted work that might be overwritten.

# Conclusion
Reverting changes in Git can be a powerful tool, whether it's for a single file, a specific patch, or an entire commit. Remember to carefully select the commit or changes you want to revert to avoid unintended modifications. Git provides the flexibility to manage your code history effectively, helping you rectify mistakes or revert to more stable versions when needed.
