---
tags:
  - fix/audit
---
# Introduction
Comparing two commits is an essential task in Git to understand the differences between various stages of your project. This guide explains how to compare two commits using Lazygit, which provides a user-friendly interface for this comparison.

# Lazygit
1. **Select the First Commit:**
   - Open Lazygit and navigate to the commit, branch, or reference you want to compare.
   - Press `shift+w` on the selected commit. This action marks the commit for comparison.

2. **Select the Second Commit:**
   - Navigate to and select the second commit you want to compare against the first one.
   - After selecting the second commit, Lazygit displays the diff in the main view.

3. **Viewing the Diff Details:**
   - Press `<enter>` to see a detailed view of the files involved in the diff.
   - This detailed view allows you to explore the specific changes between the two commits.

4. **Options in Diff Menu:**
   - Press `shift+w` again to open the diff menu for additional options like reversing the diff direction or exiting the diff mode.

5. **Exiting Diff Mode:**
   - You can exit the diff mode by pressing `<escape>`.

   ![Diff Commits in Lazygit](d53d82a1f5f9b7776df3b004bf3afd65_MD5.gif)

# Basic Terminal
To compare two commits in the terminal:

1. Use the `git diff` command with the commit hashes:
   ```bash
   git diff <commit-hash-1> <commit-hash-2>
   ```
   - Replace `<commit-hash-1>` and `<commit-hash-2>` with the actual commit hashes you want to compare.

2. The terminal will display the differences between the two commits, similar to Lazygit but in a text format.

Comparing commits in Lazygit provides a more intuitive and visual approach, while the terminal offers a more traditional, text-based method. Both are valuable tools in a developer's toolkit for understanding changes in a project.
