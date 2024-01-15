---
title: Basics of Lazygit
aliases:
  - lazygit/Overview of Lazygit
---
To run lazygit, you first need to `cd` into a git repository. Then, you can run lazygit by simply typing `lazygit` into your terminal:
```bash
cd ./to/location/of/git-repo
lazygit
```

# Lazygit UI
Now you will see the lazygit UI. It will look something like this:
- [ ] #screenshot of lazygit UI

You'll notice there are 5 panels on the left third, and then a main section on the right.
- [ ] #wireframe of 5 panels on left third, main section on right 2/3.

The 5 Left Panels are:
1. Status
2. Files
3. Local branches
4. Commits
5. Stash

## Movement and Actions
The panel in focus will be highlighted with a colored border. You can move between the panels with:
- the `left` and `right` arrow keys (or `h` and `l` for vim fans)
- `tab` and `shift+tab`
- the number keys `1-5`, corresponding to the panel number

Inside all panels, you can do the following actions:
- you can hover over items with `up` and `down` arrow keys (or `k` and `j` for vim fans)
- filter the items shown with `/`
  - `esc` to canel the filter
  - `enter` to keep the filter
- press `?`, for a help menu of all available actions on this panel
  - Each panel has different actions available.
  - Don't forget to use `/` to filter the help menu!
- press `enter` to "drill-down" into an item.
    - The specifics of what happens when you "drill-down" will depend on the panel you are in, and what item you have selected.
    - Press `esc` to go back, i.e., "drill-up"
- press `spacebar` to perform **default action** on an item.
    - on **2. Files** panel, this will toggle the staged status of the file
    - on **3. Local branches** panel, this will checkout the branch
    - on **4. Commits** panel, this will checkout the commit
    - on **5. Stash** panel, this will apply the stash
- press `page down`/`page up` - to scroll the context-aware details in the **Main Section**

### Mouse
Also, the mouse works. Click on any panel or item, to jump focus to it. Double-click to do the **default action** *(as per above)*.

- [ ] Add #svg of cute mouse icon.

## Main Section *(Context-Aware)*
The main section is context-dependent, and the information it shows you will depend on what you focused on in the left panels.

So for example, if you are focused on **2. Files** panel, and you move the cursor over a file.
- If the file is staged, then the main section will show one panel **"Staged changes"** with a diff of what you will be committing.
  - [ ] #screenshot of "Staged changes" panel

- If the file is unstaged, then the main section will show one panel **"Unstaged changes"** with a diff of what you have changed since your last commit.
  - [ ] #screenshot of "Unstaged changes" panel

- If the file is partially staged, then the main section will show two panels **"Unstaged changes"** and **"Staged changes"** each with a corresponding diff.
  - [ ] #screenshot of "Staged changes" and "Unstaged changes" panels

# Suggested Workflow for Learning Lazygit
1. The concepts and shortcuts above are the **minimal set** of knowledge you need to **memorize** to use lazygit comfortably. But once you do, lazygit will rock your world and will become your daily driver for git.
2. For the rest of the tasks in lazygit, don't make a concerted effort to memorize them. Just keep a tab open to this site, and look up stuff as needed. Do them enough times, and you'll naturally develop muscle memory for them. After a while, you'll find yourself using lazygit for more and more tasks, and you'll find yourself looking up stuff less and less.

# *See also*
- [[Overview of Panels]]
