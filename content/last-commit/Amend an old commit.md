---
tags:
  - panel/2
  - fix/audit
---

# Introduction
Amending an old commit is a useful technique in Git to revise history by modifying a previous commit. This guide will walk you through how to amend an older commit using Lazygit, a simple terminal UI for Git commands. Remember, amending commits that are already pushed to a public repository can cause issues for others who are using the same repository, so it's best used for local changes.

# Lazygit: Amending an Old Commit
## Step 1: Access the Files Panel
Begin by accessing the Files panel in Lazygit:
1. Press `2` to go to [[2. Files]].
2. Navigate through the list of changed files using `↓`/`↑` keys or a single click to hover over individual files.

## Step 2: Stage Changes
Next, stage the changes that you want to include in the old commit. This is done by selecting the files and confirming the changes.

![Staging Changes](Pasted image 20230722130208.png) *Staging changes in Lazygit*

## Step 3: Locate the Commit to Amend
In the Commits window, scroll to find the old commit you wish to amend. This commit does not have to be the most recent one.

![Selecting Commit](Pasted image 20230722130332.png) *Selecting an old commit in Lazygit*

## Step 4: Initiate Amend Process
To begin amending the commit:
1. Press `Shift+A` to start the amend process.
2. Press `Enter` to confirm the amendment.

![Amend Commit](Pasted image 20230722130415.png) *Amending a commit in Lazygit*

## Step 5: Observe Commit Hash Changes
After amending, notice that the hash of the amended commit and all subsequent commits has changed in the Commits window. This is a crucial aspect to be aware of as it indicates that the commit history has been altered.

![Commit Hash Changes](Pasted image 20230722130540.png) *Changed commit hashes after amendment in Lazygit*

## Important Note
Amending a deeper commit (not the latest one) involves Lazygit performing an internal rebase. This action will regenerate all subsequent commits with different SHA (Secure Hash Algorithm) identifiers. Be mindful that this alters the commit history and can impact shared repositories.

# Conclusion
Amending commits using Lazygit provides a visual and intuitive method to revise your Git history. However, always use this feature with the understanding that changing commit history, especially on shared branches, should be done cautiously. Happy coding!
