---
aliases:
tags:
  - fix/audit
---

# Introduction
Realizing that you need to make a small change right after committing is a common occurrence in software development. Fortunately, Git offers a way to amend the last commit. This tutorial explains how to make a quick change to your last commit without altering the project's history significantly.

# Context
Common scenarios include missing linters' guidelines, syntax errors, or small code fixes that were overlooked before committing.

# Important Gotcha
> [!warning]
> **Never amend commits that have been pushed to a public/shared branch.** Amending such commits can lead to significant issues when collaborating with others. This guide assumes the commit is local and has not been pushed.

# Amend Last Commit
## Step 1: Make Your Change
First, make the necessary small changes in your code or files.

## Step 2: Stage Your Changes
Add the files with your changes to the staging area. You can add all files, specific files, or even specific lines within files.

```bash
# To add all files
git add .

# To add specific files
git add path/fileA.txt
git add path/fileB.txt

# To add specific lines in all files
git add . -p

# To add specific lines in a specific file
git add path/fileA.txt -p
```

## Step 3: Amend the Last Commit
Now, amend the last commit. This can be done with or without changing the commit message.

```bash
# To keep the same commit message
git commit --amend --no-edit

# To change the commit message
git commit --amend
```

# Alternatives
If you prefer not to amend a commit or if the commit has already been pushed, consider these alternatives:
1. **Create a New Commit**: Simply add your changes as a new commit.
2. **Interactive Rebase**: Use `git rebase -i` to squash the new commit into the old one. This is more complex and should be done with an understanding of Git rebase.

# Conclusion
Amending the last commit for minor changes is a handy Git feature, particularly when the commit is still local. Remember to use this feature responsibly and avoid amending shared history. Happy coding!
