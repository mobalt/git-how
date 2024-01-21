---
tags:
  - fix/audit
---
# Introduction
This guide explains how to add a new remote repository in Git using Lazygit. This is particularly useful when you need to track multiple remote repositories or when you set up a new remote repository.

# Lazygit
1. Press `3` to navigate to the **3. Local Branches** panel.
2. Press `]` to switch to the next tab, which is **"Remotes"**.
3. Press `n` to initiate the creation of a new remote.
4. Enter the desired remote name when prompted.
5. Enter the remote's URL. Make sure to use the correct URL format (e.g., `https://github.com/user/repo.git` for GitHub repositories).

   Note: Ensure that the URL is correct as this is where your local repository will push to and pull from.

6. After entering the URL, confirm to complete the addition of the new remote.

   - [ ] Add #screenshot showing the remote addition confirmation.

7. You can now use this new remote for various Git operations like push, fetch, and pull.

# Basic Terminal
1. Open your terminal.
2. Navigate to your local Git repository using the `cd` command.
   ```bash
   cd /path/to/your/repo
   ```
3. Use the `git remote add` command to add a new remote. Replace `<remote-name>` with your desired remote name and `<remote-url>` with the remote's URL.
   ```bash
   git remote add <remote-name> <remote-url>
   ```
   For example:
   ```bash
   git remote add origin https://github.com/user/repo.git
   ```

4. To verify that the new remote has been added, list all the existing remotes:
   ```bash
   git remote -v
   ```
   This command will display all the remotes along with their associated URLs.

5. You can now use the new remote for pushing and pulling changes.

Remember, adding a remote in Git is a foundational task that enables collaboration and version control across different repositories. It's essential for working with team members or contributing to open-source projects.
