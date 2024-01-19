---
title: How to tell you are in a Detached State
---
# Introduction
Understanding if you're in a detached HEAD state in Git is crucial for managing your repository's history and branches effectively. This state occurs when you check out a commit, tag, or remote branch that isn't associated with a local branch. In this tutorial, we'll cover how to recognize a detached HEAD state in Lazygit.

# Lazygit
Lazygit provides visual cues to help you identify if you're in a detached HEAD state. Here are the signs to look out for:

1. **Area 1 - Repository Information:**
   - In this area, instead of showing the name of a branch, Lazygit displays a specific commit hash, indicating that you're checked out at that particular commit.
   - Example Image: ![[4c71d6860421bb8d48abcafe0341f60f_MD5.png]]
     The image demonstrates how Lazygit represents the current HEAD pointing to a specific commit hash rather than a branch name.

2. **Area 3 - Branches List:**
   - Normally, the current branch is highlighted and prefixed with a `*`. In a detached HEAD state, instead of a branch name, you'll see "HEAD detached at [SHA]".
   - Example Image: ![[8f8398cff2a3a0cfacaa92481b7f6155_MD5.png]]
     This image shows the branches panel, where the detached state is indicated by the description "HEAD detached at [SHA]".

# Basic Terminal
In the basic terminal, you can also identify a detached HEAD state:

1. Use the command:
   ```bash
   git status
   ```
   In a detached HEAD state, the output will clearly state that "HEAD is detached at [commit]".

2. Additionally, the command:
   ```bash
   git branch
   ```
   will show an entry like `* (HEAD detached at [commit])`, indicating the same state.

# Conclusion
Being in a detached HEAD state is not inherently bad, but it's essential to recognize it to avoid losing changes or creating commits that are not associated with any branch. Lazygit visually indicates this state, making it easier for users to understand their current repository status. In the terminal, standard Git commands provide clear messages about the detached HEAD state. Remember to create a new branch if you wish to keep changes made in this state.
