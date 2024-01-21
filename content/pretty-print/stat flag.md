---
title: Getting a Concise Summary of What Files Changed
tags:
  - fix/audit
---
# Introduction
This tutorial explains how to use the `--stat` flag in Git to obtain a concise summary of file changes, including the number of lines added or deleted. This flag can be particularly useful for a quick overview of changes without needing the full diff output.

# Basic Terminal
The `--stat` flag can be used with various Git commands to provide a statistical summary of changes:

1. **Using with `git log`:**
   - This shows a summary of changes for each commit in the log.
   ```bash
   git log --stat
   ```
   - You'll see a list of commits, each followed by a breakdown of files changed in that commit, along with the number of lines added and deleted.

2. **Using with `git diff`:**
   - This provides a summary of changes in the working directory compared to the last commit.
   ```bash
   git diff --stat
   ```
   - The output includes each changed file, the number of lines added or removed, and a graphical representation of these changes.

These commands are especially helpful for quickly assessing the scope of changes in a repository or in specific commits.

# Lazygit
While Lazygit doesn't have a direct equivalent to the `--stat` flag, you can visually inspect changes in files:

1. Open Lazygit and navigate to the **Files** panel.
2. Select a file to see a diff of the changes.
3. For a broader view, use the commit log in Lazygit to see the files changed in each commit.

Though not as concise as the `--stat` flag, Lazygit provides a more interactive way to explore changes in your repository.
