# Introduction
Changing the URL of a Git submodule is necessary when the source repository of the submodule has been moved or you need to switch to a different fork or version. This guide will explain how to update the submodule URL in both Lazygit and using standard Git commands.

# Lazygit: Changing Submodule URL
## Step 1: Open Lazygit in Your Repository
- Start Lazygit in the main repository that contains the submodule.

## Step 2: Access Submodule Settings
- Navigate to the submodule settings within Lazygit. This is typically done through the Submodules panel.

## Step 3: Modify Submodule URL
- Locate the submodule you wish to modify.
- Edit the URL of the submodule to the new repository address.

## Step 4: Synchronize the Submodule
- After changing the URL, synchronize the submodule to fetch and update content from the new repository.

## Step 5: Commit the Changes
- Commit the changes to record the updated submodule URL in your project's history.

# Basic Terminal: Changing Submodule URL
## Step 1: Navigate to Your Repository
- Open a terminal and go to the root directory of your main Git repository.

## Step 2: Edit the `.gitmodules` File
- The submodule URLs are stored in the `.gitmodules` file. Open this file in a text editor:

  ```bash
  vim .gitmodules
  ```

- Locate the section for the submodule you want to change and modify the `url` field to the new URL.

## Step 3: Synchronize the Changes
- After editing, synchronize the submodule:

  ```bash
  git submodule sync
  ```

- Then initialize and update the submodule:

  ```bash
  git submodule update --init --recursive
  ```

## Step 4: Commit the Changes
- Commit the updated `.gitmodules` file and any other changes:

  ```bash
  git add .gitmodules
  git commit -m "Updated submodule URL for [submodule name]"
  ```

# Conclusion
Changing the URL of a submodule allows you to keep your project linked to the correct repository. Whether using Lazygit or direct Git commands, ensure that you commit the changes so that other collaborators are also directed to the new URL when they update their submodules. This keeps everyone on the same page and avoids potential confusion or broken links.
