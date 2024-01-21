---
tags:
  - panel/4
  - fix/audit
---
# Introduction
The Autosquash workflow in Git is a method for automatically squashing 'fixup' commits into their respective original commits. This workflow is particularly useful for making small amendments or corrections to your commit history without the need to manually rebase each time. Lazygit streamlines this process with intuitive keyboard shortcuts.

# Lazygit
Here's how to use the Autosquash workflow in Lazygit:

1. **Create a Fixup Commit:**
   - Navigate to the commit you wish to amend in the **Commits** panel.
   - Press `Shift + F` to create a "fixup commit" for the selected commit. This is a new commit that will eventually be combined with the original commit.
   - Confirm the creation of the fixup commit, as prompted by the confirmation menu, shown in ![[Pasted image 20230722131237.png]].

2. **View the New Fixup Commit:**
   - After creating the fixup commit, you'll see it listed in the commits with the prefix "fixup!" as in ![[Pasted image 20230722131336.png]].

3. **Squash Fixup Commits:**
   - When you're ready to squash the fixup commits into their original commits, navigate to just below the original commit, as shown in ![[Pasted image 20230722131701.png]].
   - Press `Shift + S` to squash the above commits (including any fixup commits).
   - Confirm the squash action in the confirmation menu, depicted in ![[Pasted image 20230722131728.png]].

4. **Observe the Modified Commits:**
   - After completing the squash, observe the modified commits in your history. The `fixup!` commits should now be merged into their respective original commits, as shown in ![[Pasted image 20230722131815.png]].

# Vanilla Git
In vanilla Git, the Autosquash workflow is also available, but it requires a bit more manual intervention:

- Create a fixup commit using:
  ```bash
  git commit --fixup=<commit-hash>
  ```
  Replace `<commit-hash>` with the hash of the commit you're amending.

- When you're ready to autosquash, start an interactive rebase using:
  ```bash
  git rebase -i --autosquash <commit-hash>^
  ```
  Replace `<commit-hash>` with the hash of the commit just before the earliest commit you want to autosquash.

- Git will automatically order the fixup commits and mark them for squashing.

- Continue with the rebase process, resolving any conflicts that arise.

For more details on the vanilla Git Autosquash workflow, you can refer to resources like Thoughtbot's guide: [Autosquashing Git Commits](https://thoughtbot.com/blog/autosquashing-git-commits).

# Conclusion
The Autosquash workflow is an efficient way to clean up your commit history by squashing fixup commits into their respective original commits. Lazygit offers a streamlined and user-friendly approach to this process, while vanilla Git provides more control but requires a deeper understanding of Git commands and interactive rebase.
