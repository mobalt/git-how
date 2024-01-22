---
title: Staging all files, specific files, and specific lines
---
# Overview
This tutorial will walk you through the process of staging changes in your Git repository using Lazygit. You'll learn how to stage all files, stage entire files, and even stage specific lines within a file. This granular control can help you organize your commits effectively, especially when dealing with large changes.

# Lazygit
## Option 1: Stage All Changes
To quickly stage all your changes:
1. Press `2` to switch to the [[2. Files]] panel.
2. Press `a` to toggle all files between staged (green) and unstaged (red) status.

## Option 2: Stage Entire Files
To stage or unstage entire files:
1. Press `2` to switch to the [[2. Files]] panel.
2. Highlight the file using the `↓`/`↑` keys or the mouse.
3. Press `spacebar` (or `click`) to toggle its status:
   - Green: The file is staged.
   - Red: The file is unstaged.

- [ ] Add #screenshot of Files panel showing both staged and unstaged files.

## Option 3: Stage Specific Lines
For more control, you can stage specific lines within a file:
### Step 1: Select File to Partially Stage
1. Press `2` to switch to the [[2. Files]] panel.
2. Navigate through your files using the `↓`/`↑` keys or the mouse.
3. highlight your desired file.
4. Press `enter` to open the file's **Main Area**.

### Step 2: Stage/Unstage Changes in Main Area
The Main Area is divided into two panes:
- **Unstaged Changes**: Shows lines not yet staged.
- **Staged Changes**: Displays lines currently in stage.

Toggle focus between these panes using `tab`.

#### Unstaged Changes Panel
- `space`: Stage a line.
- `d`: Delete a line permanently (use with caution).
- `a`: Stage an entire hunk.
- `v` + `up/down`: Select multiple lines; `space` to stage them.
- `right/left`: Navigate between hunks.

>[!warning]
> The `d` key permanently deletes lines. Use it carefully to avoid losing important code.

#### Staged Changes Panel
- `space` or `d`: Unstage a line.
- `a`: Unstage an entire hunk.
- `v` + `up/down`: Select multiple lines; `space` to unstage them.
- `right/left`: Navigate between hunks.

## Monitor File Status
Watch the file status in the [[2. Files]] panel. A file with both staged and unstaged changes shows an `MM` status, with red and green colors.

# Basic Terminal
To achieve similar staging tasks in the basic terminal, you can use the following Git commands:

1. **Stage All Changes**
   ```bash
   git add .
   ```

2. **Stage Specific Files**
   ```bash
   git add <filename>
   ```

3. **Stage Specific Lines (Interactive Staging)**
   - This command opens an interactive session where you can choose specific hunks or lines to stage.
   ```bash
   git add -p <filename>
   ```

4. **Unstage Files**
   - This command unstages files without discarding changes.
   ```bash
   git reset HEAD <filename>
   ```

5. **Check Status**
   - Use this to monitor the staging status of your files.
   ```bash
   git status
   ```

# Conclusion
Mastering staging in Lazygit and the basic terminal allows for precise control over your commits. It's crucial for maintaining a clean and organized Git history. Practice these commands to enhance your version control workflow.
