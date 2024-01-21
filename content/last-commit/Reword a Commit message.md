---
tags:
  - panel/4
  - fix/audit
---

# Introduction
Sometimes after committing, you might realize that the commit message could be clearer or more descriptive. Rewording a commit message is a straightforward task in Git, and Lazygit offers an even simpler way to do it. This guide will show you how to reword a commit message using Lazygit, enhancing your commit history's clarity and understanding.

# Lazygit: Rewording a Commit Message
## Step 1: Hover Over the Commit
In Lazygit, navigate to the commit you want to reword. You can use the arrow keys to move through the commit history.

## Step 2: Choose Rewording Method
Lazygit provides two options for rewording a commit message:

### Option 1: Quick Reword
- Press `r` to reword the commit message directly within Lazygit. This option is quicker and more convenient for minor changes or fixes to the commit message.

### Option 2: Use Default Editor
- Press `R` to open the commit message in your default editor set in Git (often Vim, Nano, or another text editor). This option is better for more significant changes or if you prefer using your text editor for commit messages.

![Rewording Commit](Pasted image of Rewording Commit) *Rewording a commit in Lazygit*

# Important Notes
- **Local Commits Only**: Like amending, you should only reword commits that haven't been pushed to a public/shared branch to avoid complications in the shared repository history.
- **Impact on Commit Hash**: Rewording a commit will change its commit hash. Be aware of this if you're referencing commits by their hash in other places.

# Basic Terminal: Rewording a Commit Message
If you're not using Lazygit or prefer the classic command-line approach, here's how to reword a commit message in the terminal using Git.

## Rewording the Most Recent Commit
If the commit you want to reword is the most recent one:

1. **Open the Commit in an Editor**:
   Use the following command to open the last commit message in your default text editor:

   ```bash
   git commit --amend
   ```

2. **Edit the Message**:
   - Once the editor opens, change the commit message as needed.
   - Save and close the editor. In Vim, for instance, this is done by typing `:wq` and pressing Enter.

## Rewording an Older Commit
If you need to reword a commit that's further back in your history:

1. **Start an Interactive Rebase**:
   - Identify the commit you want to reword by finding its hash. You can use `git log` to view the commit history.
   - Start an interactive rebase for the commit before the one you want to reword:

     ```bash
     git rebase -i <commit-hash>^
     ```

2. **Mark the Commit for Rewording**:
   - In the list that appears, find the commit you want to reword.
   - Replace `pick` with `reword` (or just `r`) at the beginning of the line corresponding to your commit.
   - Save and close the file.

3. **Reword the Commit**:
   - Git will open the commit message in your default text editor.
   - Edit the message, save the file, and close the editor.

4. **Complete the Rebase**:
   - Git will now reapply the commits. If there are no conflicts, your rebase should complete automatically.

### Important Notes
- **Don't Reword Public Commits**: Avoid rewording commits that have already been pushed to a public/shared branch, as it can cause issues for anyone else working with those commits.
- **Be Cautious with Rebasing**: Interactive rebasing can be a powerful tool, but it also has the potential to significantly alter your commit history. Always ensure you understand the changes you're making.

# Conclusion
Whether using Lazygit or the basic terminal, rewording commit messages can help maintain a clear and effective project history. Choose the method that best fits your workflow and comfort level with Git commands.
