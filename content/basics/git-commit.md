---
title: Commit Staged Files
tags:
  - panel/2
---
# Overview
This guide will demonstrate how to commit staged files using both Lazygit and basic terminal commands. Understanding how to commit changes effectively is key to maintaining a well-organized and clear project history.

# Lazygit
## Committing Changes
After [[staging|staging your content]], follow these steps to commit:

1. **Access Files Panel**
   - Press `2` to navigate to the [[2. Files]] panel.

2. **Commit Options**
   - `c`: Commit the staged changes directly.
   - `C`: Open your `$EDITOR` to write a more detailed commit message.
   - `w`: Commit without running pre-commit hooks.

3. **Write Commit Message**
   - **Subject Line**: The first line (up to 50 characters) should summarize the commit's content.
   - **Body**: The second line and beyond provide details about the commit's purpose and reasoning.
   - Use `tab` to switch between the subject and body sections.
   - *See also:* [[Writing a Good Commit Message]]

4. **Finalize Commit**
   - Press `enter` to complete the commit process.

5. **Verify Commit**
   - The new commit will appear in the [[4. Commits]] panel, highlighted in a distinct color to indicate its local status and pending push to remote.

## Note on Commit Messages
   - A well-crafted commit message is vital for understanding the context and rationale behind each change.

# Basic Terminal
## Committing via Terminal
For terminal-based commits, you have two main options:

1. **Inline Commit Message**
   - Use this for quick commits:
     ```bash
     git commit -m "commit message"
     ```
   - Replace "commit message" with a concise description of your changes.

2. **Detailed Commit via `$EDITOR`**
   - For more detailed messages, default to your configured editor:
     ```bash
     git commit
     ```
   - This opens your `$EDITOR` where you can write a structured message with a subject and detailed body.

# Conclusion
Committing changes, whether through Lazygit or the terminal, is a fundamental aspect of version control. It allows for tracking changes over time and understanding the history of your project. Practice these methods to enhance your version control proficiency.
