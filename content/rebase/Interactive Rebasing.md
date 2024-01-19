---
tags:
  - panel/4
---
# Introduction
Interactive rebasing in Git is a powerful feature that allows you to modify your commit history in various ways. It can be used to change commit messages, reorder commits, squash multiple commits into one, and more. This tutorial will guide you through the process of interactive rebasing using Lazygit, a simple and intuitive Git interface.

# Lazygit
Here's how to perform interactive rebasing in Lazygit:

1. **Start the Rebase:**
   - Open Lazygit and use the `Left/Right` keys to navigate to the **Commits** panel.
   - Select the commit you want to rebase from and press `e` to start the rebase, as shown in ![[Pasted image 20230722125205.png]] and ![[Pasted image 20230722125223.png]].

2. **Configure Commit Actions:**
   - Move up and down through the commits above your selected commit.
   - Set their behavior. The default is "pick". Here are the options:
     - **pick** (`p`): Keep the commit as is.
     - **drop** (`d`): Delete this commit.
     - **edit** (`e`): Edit the commit.
     - **squash** (`s`): Merge the commit into the prior commit and append this commit's message.
     - **fixup** (`f`): Merge the commit into the prior commit and discard this commit's message.
     - **reword** (`r`): Change the commit's message (currently not functional).

3. **Moving Order of Commits:**
   - In the **Commits** window, press `Ctrl + J` or `Ctrl + K` to move commits up or down.

4. **Save the Rebase:**
   - When done, press `m` to pull up the **Rebase Options** menu as depicted in ![[Pasted image 20230722125632.png]].
   - The before and after state of your commit history can be observed in ![[Pasted image 20230722125721.png]] and ![[Pasted image 20230722125742.png]].

5. **Handle Merge Conflicts:**
   - Be aware that this process might result in merge conflicts that you'll need to resolve manually.

6. **Additional Resources:**
   - For more insights, refer to the description by the Lazygit creator on interactive rebasing at Opensource.com.

# Basic Terminal
To perform interactive rebasing in the terminal:

1. Start the interactive rebase:
   ```bash
   git rebase -i <commit-hash>^
   ```
   Replace `<commit-hash>` with the hash of the commit just before the one you want to start rebasing from.

2. In the interactive rebase editor, set the desired action for each commit (pick, squash, fixup, etc.).

3. Save and exit the editor, and follow the prompts to complete the rebase.

4. Resolve any merge conflicts that arise during the process.

# Conclusion
Interactive rebasing in Lazygit offers a user-friendly way to alter your commit history, providing a visual and intuitive interface. The terminal approach, while more text-based, offers the same level of control. Interactive rebasing is a powerful tool but should be used with caution, especially on shared branches or after changes have been pushed to a remote repository.
