---
tags:
  - panel/4
  - fix/audit
---
# Introduction
Git bisect is a vital tool for diagnosing the introduction of issues in your codebase. This guide covers how to use git bisect both in Lazygit and through the basic terminal, offering flexibility depending on your preferred workflow.

# Lazygit
1. **Accessing the Commits View:**
   - Navigate to the commits view in Lazygit, typically under [[4. Commits]].

2. **Starting Git Bisect:**
   - Press `b` on a commit to mark it as good or bad, initiating the git bisect process.

3. **Identifying the Problematic Commit:**
   - Continue marking commits as good or bad based on whether the issue is present. Lazygit automates the checkout process for you.
   - Repeat until the commit causing the issue is identified.

   ![Git Bisect in Lazygit](d7d8e597f017be21502235d0645112b9_MD5.gif)

# Basic Terminal
1. **Starting Git Bisect:**
   - In your terminal, start git bisect:
     ```bash
     git bisect start
     ```

2. **Marking Bad Commit:**
   - Mark the current HEAD or any known bad commit:
     ```bash
     git bisect bad
     ```

3. **Marking Good Commit:**
   - Mark a commit where the issue was not present:
     ```bash
     git bisect good <commit-hash>
     ```
   - Replace `<commit-hash>` with the hash of the known good commit.

4. **Narrowing Down the Commit:**
   - Git will automatically check out a commit for testing. Test the code to see if the issue is present.
   - Mark this commit as good or bad accordingly:
     ```bash
     git bisect good
     ```
     or
     ```bash
     git bisect bad
     ```
   - Git will continue to guide you to different commits based on your input.

5. **Ending the Bisect:**
   - Once the problematic commit is found, end the bisect session:
     ```bash
     git bisect reset
     ```
   - This command returns your repository to its pre-bisect state.

# Conclusion
Whether using Lazygit for a more graphical approach or sticking to the basic terminal for a more traditional method, git bisect is an incredibly effective way to track down the specific commit that introduced an error or bug in your project.
