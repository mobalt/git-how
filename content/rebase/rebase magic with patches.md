---
tags:
  - panel
---

### Rebase Magic (Custom Patches)

# Introduction
Rebase magic in Git, especially with custom patches, allows for sophisticated manipulation of your commit history. This can be particularly useful for cleaning up commits, removing unnecessary changes, or even splitting a large commit into smaller ones. Lazygit provides an intuitive interface to perform these tasks with ease.

# Lazygit
Here's how to use rebase magic with custom patches in Lazygit:

1. **Select the Commit:**
   - Open Lazygit and navigate to the **Commits** panel.
   - Scroll to the commit you want to modify and press `enter` to view its files.

2. **Focus on the File and Create a Patch:**
   - Navigate to the specific file you wish to edit and press `enter` to focus on the patch.
   - Use `space` to select lines for your custom patch. In this case, add the redundant comment line to your custom patch.

3. **Access Custom Patch Options:**
   - Press `Ctrl + P` to open the custom patch options.
   - Choose the option to "remove the patch from the current commit". This will create a new commit without the selected lines.

4. **Finalize the Changes:**
   - After selecting to remove the patch from the current commit, Lazygit will perform the necessary actions. This may include an interactive rebase behind the scenes.
   - Follow any additional prompts to resolve conflicts or finalize the rebase.

5. **Learn More:**
   - For a more detailed guide, refer to the "Rebase magic Youtube tutorial" provided by Lazygit's creator. [Watch the tutorial here](https://youtu.be/4XaToVut_hs).
   - Also, check out this visual demonstration: [Rebase Magic with Custom Patches](https://github.com/jesseduffield/lazygit/blob/assets/demo/custom_patch-compressed.gif).

# Basic Terminal
To perform a similar action in the terminal:

1. Start an interactive rebase:
   ```bash
   git rebase -i <commit-hash>^
   ```
   Replace `<commit-hash>` with the hash of the commit just before the one you want to edit.

2. Mark the commit you want to edit with `edit` instead of `pick`.

3. When Git pauses at that commit, manually edit the file to remove the redundant lines.

4. Stage the changes and amend the commit:
   ```bash
   git add <file>
   git commit --amend
   ```

5. Continue the rebase:
   ```bash
   git rebase --continue
   ```

# Conclusion
Using rebase magic with custom patches in Lazygit allows for refined control over your commit history, making it easier to maintain a clean and organized repository. The terminal approach offers more control but requires familiarity with Git's rebase and commit amendment commands. Remember, modifying historical commits should be done cautiously, particularly in shared branches or repositories.
