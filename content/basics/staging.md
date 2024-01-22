---
title: Staging all files, specific files, and specific lines
---
# Overview
This tutorial will walk you through the process of staging changes in your Git repository using Lazygit. You'll learn how to stage all files, stage entire files, and even stage specific lines within a file. This granular control can help you organize your commits effectively, especially when dealing with large changes.

# Lazygit
## Step 1: Navigate to Files Panel
To start, you need to view your file changes in Lazygit:
1. Press `2` to switch to the [[2. Files]] panel.
2. Navigate through your files using the `↓`/`↑` keys or the mouse.

## Option 1: Stage All Changes
To quickly stage all your changes:
1. Press `a` to toggle all files between staged (green) and unstaged (red) status.

## Option 2: Stage Entire Files
To stage or unstage entire files:
1. Highlight the file using the `↓`/`↑` keys.
2. Press `spacebar` (or `click`) to toggle its status:
   - Green: The file is staged.
   - Red: The file is unstaged.

- [ ] Add #screenshot of Files panel showing both staged and unstaged files.

## Option 3: Stage Specific Lines
For more control, you can stage specific lines within a file:
### Step 3: Select File to Partially Stage
1. In the Files panel, navigate to and highlight your desired file.
2. Press `enter` to open the file's **Main Area**.

### Step 4: Stage/Unstage Changes in Main Area
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

### Step 5: Monitor File Status
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
   ```bash
   git add -p <filename>
   ```
   - This command opens an interactive session where you can choose specific hunks or lines to stage.

4. **Unstage Files**
   ```bash
   git reset HEAD <filename>
   ```
   - This command unstages files without discarding changes.

5. **Check Status**
   ```bash
   git status
   ```
   - Use this to monitor the staging status of your files.

# Conclusion
Mastering staging in Lazygit and the basic terminal allows for precise control over your commits. It's crucial for maintaining a clean and organized Git history. Practice these commands to enhance your version control workflow.
