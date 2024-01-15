---
title: "Stage: Specific lines"
tags:
  - panel/2
aliases:
  - How to Partially Stage a File
---
# Lazygit
1. Press `2`, to go to [[2. Files]]
2. Select a file with `up`/`down`, or mouse click
3. Press `enter` to drill-down into the file you want to partially stage.
    - This will move focus to the **Main Area**.
4. The **Main Area** will have one or both of these panes:
	- **Unstaged changes** - lines that are not staged
	- **Staged changes** - lines that are staged
5. Use `tab` to toggle focus between **Unstaged changes** and **Staged changes** panes.
6. Inside the **Unstaged changes**, press
	-  `space` to add ("stage") a line.
	- `d` to completely delete a line. This is permanent.
		- e.g., if you accidentally left a **console.log** in the middle of your code
	- `a` - to stage entire hunk
	- `v` - to visually stage a range (multiple lines), `up/down` keys to go up or down. Then `space` to stage.
	- `right/left` - to go to next/previous hunk, if any
7. Inside the **Staged changes**, press
	- `space` or `d` - to unstage a line
    - `a` - to unstage entire hunk
    - `v` - to visually unstage a range (multiple lines), `up/down` keys to go up or down. Then `space` to unstage.
    - `right/left` - to go to next/previous hunk, if any
8. Notice that in the [[2. Files]] panel, the file you are working on will be shown as `MM` (colored red, then green) to signal that it is partially staged.

- [ ] Add #screenshot of partially staged file in Files panel