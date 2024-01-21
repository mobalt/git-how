---
aliases:
  - Change the message on my Last Commit
tags:
  - fix/audit
---

# Introduction
Changing the message of the most recent commit is a common task in Git, especially if you've made a typo or left out important information. This guide will show you how to amend the last commit message and also cover how to abort the process or undo the amendment if needed.

# Git: Rewriting the Last Commit Message
## Step 1: Amend the Commit
In your Git repository, use the following command to start amending your last commit:

```bash
git commit --amend
```

## Step 2: Change the Commit Message
- Once you run this command, your default text editor will open with the last commit message.
- Edit the message to what you want it to be.
- Save and close the editor (for example, in Vim, type `:wq` and press Enter).

## Abort Amendment
If you're in the editor and decide not to change the commit message:
- To keep the original message: don't make any changes, then save and close the editor.
- To cancel the amend: delete the commit message, save, and close the editor. This will abort the commit amendment process.

## Undoing an Amendment
Since `git commit --amend` creates a new commit with a different SHA (commit hash), undoing it involves a few steps:

### Find the Original Commit SHA
1. Use `git reflog` to find the SHA of the commit before the amend.
2. Look for the entry just before the amend. The reflog will have a message like "amend commit: your commit message."

### Reset to the Original Commit
1. Once you have the original SHA, reset your branch to that commit:

   ```bash
   git reset --hard <original-SHA>
   ```

2. This will reset your branch to the state before the amend, including the original commit message.

### Warning
- **Be Careful with `git reset --hard`**: This command can discard changes in your working directory and index. Always ensure you have no uncommitted changes before using it.
- **Local Commits Only**: Avoid amending commits already pushed to a public/shared branch, as this can cause problems for others working on the project.

# Conclusion
Amending the last commit message is straightforward in Git, but always be mindful of the state of your repository and the implications of changing commit history. Remember, it's best to only amend commits that are local and not yet pushed to a shared repository.
