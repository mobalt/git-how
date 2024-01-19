---
tags:
  - panel/2
---
# Introduction
Resolving merge conflicts is a common task in version control. Lazygit provides an intuitive interface for addressing these conflicts. This guide will walk you through the process of resolving merge conflicts using Lazygit.

# Lazygit
1. **Navigate to Changed Files:**
   - Press `2` to open the [[2. Files]] panel.
   - Use `↓`/`↑` keys or a `single click` to hover over individual files that have conflicts.

2. **Access the Diff Panel:**
   - Press `enter` on a conflicted file to open the **Diff** panel in the **Main area**.
   - This panel shows the differences between the conflicting versions of the file.

3. **Resolve Each Conflict:**
   - For every conflict section (hunk) in the file, you have options to resolve it:
     - Press `b` to keep both versions. This will merge both sides of the conflict into the file.
     - Scroll to the version you want to keep (either HEAD or incoming change) and press `space` to choose that version.

4. **Complete the Conflict Resolution:**
   - After resolving all conflicts in a file, a prompt **all merge conflicts resolved. Continue?** will appear.
   - Press `enter` to confirm that all conflicts are resolved.

5. **Repeat for Other Files:**
   - Repeat steps 2 to 4 for each file with conflicts until all conflicts are resolved.

6. **Final Steps:**
   - Once all conflicts are resolved, you can continue with your Git workflow (e.g., completing a merge or rebase).

# Additional Tips
- **Review Changes Carefully:** Ensure that the merged code is functional and makes sense in the context of your project.
- **Commit Resolution:** After resolving conflicts, don't forget to commit the changes to finalize the resolution.
- **Backup Before Resolving:** It's a good practice to backup important files before resolving conflicts, especially for complex merges.

Using Lazygit for conflict resolution provides a visual and user-friendly way to handle these challenges, making it easier to understand and resolve conflicts effectively.
