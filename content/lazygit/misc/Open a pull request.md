---
tags:
  - panel/4
  - fix/audit
---
# Introduction
Opening a pull request is a key step in collaborative coding workflows. Lazygit simplifies this process by integrating directly with your web browser. This guide will demonstrate how to open a pull request from Lazygit.

# Lazygit
1. **Navigate to the Branch:**
   - In Lazygit, go to the branch you want to create a pull request for. This is typically done in the branches panel, accessible under [[4. Branches]].

2. **Opening a Pull Request:**
   - Once you've selected the branch, press `o`. This action will trigger Lazygit to open your default web browser.
   - Your browser will navigate to the corresponding repository hosting service (like GitHub, GitLab, etc.) and start the process of opening a pull request with the selected branch.

3. **Completing the Pull Request:**
   - In the browser, you'll see the pull request form pre-filled with the details from your branch.
   - Fill out any additional details required for the pull request, such as the title, description, reviewers, and any specific pull request templates your repository might use.

   ![Lazygit Pull Request](lazygit_7.png)

# Basic Terminal
While Lazygit offers a convenient way to open pull requests, you can also initiate this process manually from the terminal:

1. **Push Your Branch:**
   - First, ensure your branch is pushed to the remote repository:
     ```bash
     git push origin <branch-name>
     ```

2. **Opening Pull Request via Web:**
   - After pushing, visit the repository's webpage on your hosting service (GitHub, GitLab, etc.).
   - Navigate to the "Pull Requests" or "Merge Requests" section.
   - Click the button to create a new pull request and select your branch.

3. **Using Hub or GitLab CLI:**
   - For GitHub users, the [Hub](https://hub.github.com/) tool allows you to open a pull request directly from the terminal.
   - Similarly, GitLab users can utilize the [GitLab CLI](https://docs.gitlab.com/ee/user/project/merge_requests/creating_merge_requests.html) for this purpose.

# Conclusion
Lazygit streamlines the process of opening pull requests by integrating directly with your web browser, offering a seamless transition from coding to collaboration. For those who prefer the command line, manual methods or specialized tools like Hub and GitLab CLI also facilitate this essential step in modern software development workflows.


![[lazygit_7.png]]
