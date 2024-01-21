---
tags:
  - fix/audit
---
# Introduction
Writing good commit messages is an essential practice in collaborative software development. It not only helps in understanding the changes made but also facilitates effective communication among team members. This guide will provide best practices for crafting meaningful commit messages, applicable in any Git environment, whether you're using a tool like Lazygit or the basic terminal.

# Writing a Good Commit Message

## 1. Separate Subject from Body
   - Start with a concise subject line (50 characters or less) summarizing the change, followed by a blank line, then a more detailed explanation if needed.

## 2. Use the Imperative Mood in the Subject Line
   - Write the subject line as if you are giving a command or instruction, e.g., "Fix bug in payment processing," which reflects what the commit will do once applied.

## 3. Be Clear and Descriptive
   - The message should clearly describe what the commit does, not just what was done. Avoid vague descriptions like "fixed stuff" or "updates."

## 4. Explain the Context and Reasoning
   - Where necessary, include the reasons for your changes and any considerations that informed your decisions. This helps future maintainers understand your thought process.

## 5. Mention Associated Issues or Ticket Numbers
   - If the commit is related to a specific issue or ticket, include the reference number in the commit message, e.g., "Fixes #123."

## 6. Keep It Short and Focused
   - Each commit should contain a single logical change. Avoid bundling multiple unrelated changes in one commit.

## 7. Use Bullet Points for Multiple Changes
   - When listing multiple changes, use bullet points for clarity:
     ```
     - Improve user login performance
     - Fix crash in user profile update
     - Update localization files for French and German
     ```

## 8. Avoid Redundant Phrases
   - Skip unnecessary words like “added” or “changed” as Git shows these actions in the commit history.

## 9. Capitalize the Subject Line
   - Start the subject line with a capital letter.

## 10. Do Not End the Subject Line with a Period
   - The subject line should not end with a period.

# Conclusion
Effective commit messages serve as a historical record of changes, making it easier to understand the development process and rationale behind decisions. These best practices will enhance the quality and usefulness of your commit messages, contributing to a more organized and accessible project history. Whether using Lazygit or terminal commands, the importance of a well-written commit message remains paramount in collaborative Git workflows.
