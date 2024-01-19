---

# Overview
This tutorial will help you understand how to use Git's powerful `reflog` feature and Lazygit's undo capabilities. `git reflog` is often described as a magic time machine in Git. It's a lifesaver when you've made changes that you regret or want to revert. We'll also cover how to do similar actions in Lazygit, a simple terminal UI for Git commands.

# Lazygit

### Undoing Actions in Lazygit

1. **Undo the Last Action**:
   - In Lazygit, you can undo the last action by pressing `z`.
   - To redo an undone action, press `Ctrl+z`.
   - Note: This undo functionality is limited to commits and branch changes. It does not affect working tree changes or stashed items.
   - Here's a visual demonstration: [Undo Demo](https://github.com/jesseduffield/lazygit/blob/assets/demo/undo-compressed.gif).

### Using the Reflog Tab

2. **Accessing the Reflog Tab**:
   - Switch to the reflog tab in Lazygit by pressing `]`.
   - This tab shows a list of recent Git actions, similar to what you see in the commits panel.

3. **Restoring an Older Version**:
   - Navigate through the list using the `↓` and `↑` keys.
   - To restore an older version of your project, select the desired entry and press the `space` key.
   - This action is akin to performing a `git reset` to a specific state from the reflog.

# Basic Terminal

### Understanding `git reflog`

1. **Viewing the Reflog**:
   - Run `git reflog` in your terminal.
   - This command displays a list of recent actions in Git across all branches, each with a unique index `HEAD@{index}`.
   - Example output:
     ```
     f5816a18 HEAD@{2}: rebase -i (start)
     791a1f1b HEAD@{3}: commit
     819d66fc HEAD@{4}: checkout
     ```
   - Identify the state you want to revert to.

2. **Using the Reflog to Undo Changes**:
   - To revert to a specific state, use `git reset`. You can specify either the commit hash or the `HEAD@{index}`.
   - For example:
     ```
     git reset --hard 791a1f1b
     # or
     git reset --hard HEAD@{3}
     ```
   - This action will reset your project to the state it was in at the specified point in the reflog.

### Practical Applications

3. **Common Use Cases**:
   - Recover lost commits or branches.
   - Undo a problematic rebase, merge, or other Git operations.
   - Rollback to a point before an error was introduced.

---

Remember, while `git reflog` is powerful, it should be used with caution, especially with commands like `git reset --hard`, as they can alter your project history. Always make sure you're reverting to the correct state to avoid unintended data loss.
