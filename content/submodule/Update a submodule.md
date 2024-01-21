---
tags:
  - fix/audit
---
# Introduction
Updating a submodule is essential when you want to track the latest changes or a specific commit from the submodule's repository. This process involves fetching the latest changes and updating your working copy to point to a new commit within the submodule.

# Lazygit
## Step 1: Open Lazygit in Your Main Repository
- Start Lazygit within the main Git repository that contains the submodule.

## Step 2: Navigate to the Submodule
- In Lazygit, go to the section where submodules are listed.

## Step 3: Update the Submodule
- Select the submodule you wish to update.
- Use the designated command or key binding in Lazygit to update the submodule. This typically involves fetching the latest changes from the remote and checking out the desired commit.

## Step 4: Commit the Submodule Update
- After updating the submodule, a new commit hash will be checked out.
- Commit these changes in your main repository to track the updated state of the submodule.

# Basic Terminal: Updating a Submodule
## Step 1: Navigate to Your Main Repository
- Open a terminal and change directories to the root of your main Git repository.

## Step 2: Update the Submodule
- Use the following commands to update your submodule:

  ```bash
  git submodule update --init --recursive
  ```

  - `--init` initializes the submodule if it hasn't been initialized already.
  - `--recursive` ensures that any submodules within the submodule are also updated.

## Step 3: Fetch and Checkout a Specific Commit (Optional)
- If you want to update the submodule to a specific commit:
  - First, navigate to the submodule directory:

    ```bash
    cd path/to/submodule
    ```

  - Fetch the latest changes and checkout the specific commit:

    ```bash
    git fetch
    git checkout <specific-commit-hash>
    ```

  - Return to the root of your main repository:

    ```bash
    cd -
    ```

## Step 4: Commit the Changes in the Main Repository
- Stage and commit the changes to record the updated state of the submodule in your main repository:

  ```bash
  git add path/to/submodule
  git commit -m "Updated submodule to <specific-commit-hash>"
  ```

# Conclusion
Updating a submodule is a critical step in maintaining the integrity and currency of your project dependencies. Whether using Lazygit for a more intuitive interface or standard terminal commands for direct control, it's important to regularly update your submodules and commit these changes to track the evolution of your project accurately.
