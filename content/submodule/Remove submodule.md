# Introduction
Removing a submodule from a Git repository involves more than just deleting the submodule's directory. It requires changes to the Git configuration and index. This guide will walk you through the steps to properly remove a submodule using Lazygit and the basic terminal.

# Lazygit: Removing a Submodule
## Step 1: Open Lazygit in Your Repository
- Launch Lazygit in the main repository that contains the submodule you want to remove.

## Step 2: Navigate to the Submodule
- Go to the Submodules section in Lazygit and select the submodule you wish to remove.

## Step 3: Remove the Submodule
- Use the designated key or command within Lazygit to remove the selected submodule. This action should remove the submodule from the working directory and staging area.

## Step 4: Commit the Removal
- After removing the submodule, commit the changes to finalize the removal process. This includes deleting the submodule reference in the `.gitmodules` file and the submodule's entry in the `.git/config` file.

# Basic Terminal: Removing a Submodule
## Step 1: Delete the Submodule Files
- In the terminal, navigate to the root of your main repository.
- Delete the submodule's directory:

  ```bash
  rm -rf path/to/submodule
  ```

## Step 2: Remove Submodule References
- Edit the `.gitmodules` file to remove the submodule's entry:

  ```bash
  git config --file .gitmodules --remove-section submodule.path/to/submodule
  ```

- Also, remove the submodule's entry from `.git/config`:

  ```bash
  git config --remove-section submodule.path/to/submodule
  ```

## Step 3: Unstage the Submodule and Commit
- Unstage the submodule:

  ```bash
  git rm --cached path/to/submodule
  ```

- Commit the changes to finalize the removal:

  ```bash
  git commit -m "Removed submodule [submodule name]"
  ```

## Step 4: Clean Up
- Optionally, run `git rm --cached path/to/submodule` if the submodule's directory still exists in the index.
- Execute `git clean -fd` to remove untracked files and directories, including the now-removed submodule directory.

# Conclusion
Whether using Lazygit for a more visual approach or standard terminal commands for more control, removing a submodule requires careful attention to both the working directory and Git configuration. Ensure that all references to the submodule are properly removed and the changes are committed to maintain a clean and accurate repository state.
