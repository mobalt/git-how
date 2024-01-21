---
tags:
  - panel/4
  - fix/audit
---
# Introduction
Viewing detailed information about a specific commit is an essential aspect of navigating and understanding your project's history in Git. Using Lazygit, you can easily explore the changes made in each commit. This guide will show you how to access and view these details within Lazygit.

# Lazygit: Viewing Commit Details
## Step 1: Select the Commit
In the **Commits** window of Lazygit:
1. Hover over the commit you're interested in.
2. Press `Enter` or `double-click` on the commit.

## Step 2: Explore Commit Changes
Once you select a commit:
- The area in the Lazygit interface labeled **4. Commits** will transform into the **4.1.2. Diff files** menu.
- This new view presents a list of individual files that were modified in the selected commit.
- You can navigate through these files to see the specific changes made in each one.

![Commit Files Window](Pasted image 20230722130754.png) *Viewing commit files in Lazygit*

## Step 3: Returning to Commit List
To go back to the list of commits:
- Simply press `Escape`.
- This will return you to the **4. Commits** window where you can continue to browse through other commits.

# Basic Terminal: Viewing Commit Details
If you prefer to use the command line without Lazygit, you can view details about a commit using Git commands:

1. **Find the Commit Hash**: Use `git log` to find the hash of the commit you want to inspect.

2. **Show Commit Details**: Run the following command, replacing `<commit-hash>` with the actual hash:

   ```bash
   git show <commit-hash>
   ```

   - This command displays the commit's details, including the diff of the changes made.

3. **Navigate the Output**: If your terminal uses a pager like `less`, you can navigate through the output using arrow keys and exit by pressing `q`.

# Conclusion
Whether using Lazygit's intuitive interface or standard Git commands in the terminal, viewing the details of a commit is a valuable skill for managing and understanding your project's history. It allows you to track changes, understand past decisions, and effectively collaborate with others.
