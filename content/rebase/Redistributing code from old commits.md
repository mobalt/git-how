---
tags:
  - panel/4
---
# Introduction
Redistributing code from old commits is a sophisticated Git operation that allows you to rearrange changes made in your repository's history. This can be useful for cleaning up commits, separating features, or fixing mistakes. Lazygit provides a user-friendly interface to handle this process with custom patches.

# Lazygit
Follow these steps to redistribute code from old commits in Lazygit:

1. **Navigate to Commit Files:**
   - Open Lazygit and go to the **Commits** panel.
   - Scroll to the commit of interest and press `enter` to open the **Commit Files** window.

2. **Select File for Modification:**
   - In the **Commit Files** window, select the file you want to modify and press `enter`.
   - This opens the **Add Lines/Hunks to Patch** window.
   - Scroll to the lines with changes you want to move and press `space` to add them to the custom patch on the right window, as shown in the image ![[Pasted image 20230722134714.png]].

3. **Apply the Custom Patch:**
   - Go back to the **Commits** window by pressing `esc` twice.
   - Scroll to the commit where you want to apply the custom patch, as indicated in ![[Pasted image 20230722135012.png]].
   - Press `Ctrl + P` to bring up the **Patch Options** menu, shown in ![[Pasted image 20230722135101.png]].
   - Select "**move patch to selected commit**" and press `enter`.

4. **Observe the Changes:**
   - After applying the patch, observe the changes in your commit history, as illustrated in ![[Pasted image 20230722135233.png]].

### Creating Custom Patches

Custom patches are a core feature in Lazygit, allowing you to interactively modify your commit history:

- To create a custom patch, navigate within a commit and use `space` to toggle entire files or specific lines/hunks for the custom patch.
- The custom patch you're building is displayed as a separate panel, as shown in ![[custom-patch.png]].
- To access the custom patch menu, type `Ctrl + P`. This menu, depicted in ![[custom-patch-menu.png]], offers various options, such as resetting the patch, applying it, or creating a new commit with the changes.

# Basic Terminal
In the terminal, redistributing changes from old commits can be more complex:

1. Start an interactive rebase:
   ```bash
   git rebase -i <commit-hash>^
   ```
   Choose the commit just before the one you want to edit.

2. Mark the commit with `edit`.

3. Make the necessary code changes and commit them:
   ```bash
   git add <file>
   git commit --amend
   ```

4. Continue the rebase process:
   ```bash
   git rebase --continue
   ```

5. Repeat these steps for each commit you want to modify.

# Conclusion
Redistributing code from old commits using Lazygit's custom patches is a powerful way to refactor your commit history. While Lazygit provides a visual and interactive approach, the terminal commands offer a more traditional method but require careful handling to avoid errors. Remember, modifying historical commits should be approached with caution, especially in shared repositories.
