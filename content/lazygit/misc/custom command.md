---
tags:
  - panel
  - fix/audit
---
# Introduction
Lazygit's custom command system offers a high degree of flexibility, allowing users to tailor their Git experience to their specific needs. This guide highlights how to define and use custom commands in Lazygit, using the example of emulating a built-in branch checkout action.

# Lazygit Custom Commands
1. **Understanding Custom Commands:**
   - Lazygit allows you to define custom commands for frequent operations or complex Git commands that aren't built into Lazygit.
   - You can configure these commands via Lazygit's configuration file or through the UI.

2. **Example - Custom Branch Checkout:**
   - A custom command can be set up to emulate the branch checkout action.
   - Once defined, this command can be triggered within Lazygit to checkout branches in a way that suits your workflow.

   ![Custom Command in Lazygit](98c2d64ed4259b6252afaa436957bef0_MD5.gif)

3. **Using `:` for External Commands:**
   - Lazygit also allows the execution of external Git commands directly.
   - Press `:` within Lazygit to enter an external command. This feature is useful for running Git commands that are not natively supported in Lazygit’s UI.

4. **Defining Custom Commands:**
   - Custom commands are defined in Lazygit's configuration file. You can specify the keybindings, descriptions, and the actual Git command that should be executed.
   - For more details on setting up custom commands, refer to the [Custom Command Keybindings Documentation](https://github.com/jesseduffield/lazygit/blob/master/docs/Custom_Command_Keybindings.md).

# Basic Terminal
While Lazygit offers a user-friendly interface for custom commands, you can also create aliases or scripts in your terminal for similar functionality:

1. **Creating Aliases:**
   - In your shell's configuration file (e.g., `.bashrc` or `.zshrc`), you can create aliases for frequently used Git commands.
   - Example:
     ```bash
     alias gco='git checkout'
     ```
   - This alias allows you to use `gco` as a shorthand for `git checkout`.

2. **Scripting Complex Commands:**
   - For more complex Git operations, consider writing shell scripts that encapsulate multiple Git commands or operations.
   - These scripts can be saved and executed from anywhere in your system, offering a level of customization similar to Lazygit's custom commands.

# Conclusion
Lazygit's custom command system provides an excellent way to enhance your Git workflow, making frequent operations more accessible and tailored to your needs. For those who prefer the command line, aliases and scripts in the terminal offer a powerful alternative for customizing your Git experience.
