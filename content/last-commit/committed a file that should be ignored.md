---
tags:
  - fix/audit
---

# Introduction
Accidentally committing files that should be ignored, such as large files or files containing sensitive information, is a common scenario in Git. This tutorial covers how to remove such files from your commit history in your local repository and, if necessary, from a remote repository.

# Context
You might need to remove a file from Git for various reasons:
- **Size Issues**: Large files, like a 1.5GB video file, can bloat the repository.
- **Sensitive Data**: Files containing secrets or sensitive information should not be in a public repository.

# Removing Commit from Local Git
## Assumptions
- You have not yet pushed (`git push`) the undesirable commit to a remote repository.

## Removing from the Last Commit
### Step 1: Stage the Removal of the File
First, remove the file from the staging area and index without deleting it from your file system:

```bash
git rm --cached bigfile.mpv
```

### Step 2: Amend Your Last Commit
Amend the commit to exclude the file. This will open an editor for you to modify the commit message if necessary:

```bash
git commit --amend
```

### Step 3: Update .gitignore (Optional)
To prevent the file from being accidentally committed again, add it to your `.gitignore` file:

```bash
echo "bigfile.mpv" >> .gitignore
git add .gitignore
git commit --amend
```

## Removing from a Deeper Commit
For files committed in earlier commits (not the most recent one), you would typically use an interactive rebase or squash. This process is more complex and will be covered in a future update.

# Removing Commit from Origin
## Important Considerations
- **Security Implications**: If the committed file contains secrets or sensitive information, assume that it has been compromised. Rotate the secrets immediately.
- **Collaboration Warning**: Inform your collaborators. If they don't pull the changes with `git pull --rebase`, there's a risk they might repush the unwanted file.

## Steps to Remove Commit from Origin
This section will be updated with detailed instructions on how to remove the commit from a remote repository.

# Conclusion
Carefully managing your commits and understanding how to rectify mistakes is crucial in Git. Remember to update your `.gitignore` file regularly and communicate with your team to ensure smooth collaboration. Stay tuned for updates on handling deeper commits and remote repository changes.
