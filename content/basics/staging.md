---
title: Staging all files, specific files, and specific lines
---
This guide focuses on how to partially stage files – a process that allows you to select specific changes in a file to include in your next commit. This is particularly useful for breaking up large sets of changes into smaller, more manageable commits.

# Lazygit
## Step 1: Navigate to Files Panel
Start by opening the Files panel in Lazygit to view your file changes:
1. Press `2` to switch to the [[2. Files]] panel.
2. Use `↓`/`↑` keys, to navigate through the list of changed files.

## Option 1: Stage All Changes
Sometimes, you're in a rush, and just want to stage all your changes into the next commit.
3. Press `a`, to toggle between staging *(green)* and unstaging *(red)* all files.

## Option 2: Stage Entire Files
3. Use `spacebar`(or `click`) to toggle between
    1. *(green)* Add entire file to Stage
    2. *(red)* Remove entire file from Stage

- [ ] Add #screenshot of Files panel with multiple staged and unstaged files
## Option 3: Stage only Specific Lines
Sometimes you want to partially stage files – a process that allows you to select specific changes in a file to include in your next commit. This is particularly useful for breaking up large sets of changes into smaller, more manageable commits.

### Step 3: Select File to Partially Stage
Once in the Files panel, choose a file to partially stage:
1. Highlight the desired file by navigating to it.
2. Press `enter` to drill down into the selected file. This will shift focus to the **Main Area**.

### Step 4: Stage/Unstage Changes in Main Area
In the Main Area, you will encounter two key panes:
- **Unstaged Changes**: Displays lines of code that have not been staged yet.
- **Staged Changes**: Shows lines of code that have already been staged.

Use `tab` to toggle focus between these two panes, to selectively stage or unstage changes.

#### Unstaged Changes Panel
Use the following keys:
  - `space` - to stage a line.
  - `d` - to delete a line ***permanently***.
	  - Useful for removing accidental changes like a stray `console.log`.
  - `a` - to stage an entire hunk.
  - Press `v` then use `up/down` to select multiple lines, and `space` to stage them.
  - Use `right/left` to navigate between hunks.
>[!warning]
> Be cautious when permanently deleting lines using `d` in the **Unstaged Changes** pane. This action cannot be undone and might lead to loss of important code.

#### Staged Changes Panel
Use the following keys:
  - `space` or `d` - to unstage a line.
  - `a` - to unstage an entire hunk.
  - Press `v` then use `up/down` to select multiple lines, and `space` to unstage them.
  - Use `right/left` to navigate between hunks.

### Step 5: Monitor File Status
As you stage and unstage changes, notice the status of the file in the [[2. Files]] panel. A partially staged file is indicated by an `MM` status, colored red then green.


# Conclusion
Partially staging files in Lazygit is a powerful feature that provides granular control over what changes go into your commits. This allows for a cleaner, more organized commit history. Remember, careful staging can make a significant difference in maintaining a clear and manageable Git history.
