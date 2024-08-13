# git-5

## config:

The `git config` command is used to configure Git settings at different levels: system-wide, user-specific (global), or project-specific (local). Here are some commonly used `git config` commands:

#### Setting User Information

1.  **Set Your Name:**

    ```bash
    git config --global user.name "Your Name"
    ```

    This command sets your name, which will be attached to your commits.
2.  **Set Your Email:**

    ```bash
    git config --global user.email "your.email@example.com"
    ```

    This command sets your email address, which will also be attached to your commits.

#### Viewing Configuration

3.  **View All Configuration:**

    ```bash
    git config --list
    ```

    This command lists all the configuration settings, combining system, global, and local configurations.
4.  **View Specific Configuration:**

    ```bash
    git config user.name
    ```

    This will show the value of the `user.name` setting.

#### Configuring Editor

5.  **Set Default Text Editor:**

    ```bash
    git config --global core.editor "code --wait"
    ```

    This sets Visual Studio Code as your default editor. Replace `"code --wait"` with `"vim"`, `"nano"`, or another editor of your choice.

#### Configuring Aliases

6.  **Set an Alias:**

    ```bash
    git config --global alias.co checkout
    ```

    This creates an alias `co` for the `checkout` command, allowing you to use `git co` instead of `git checkout`.

#### Configuring Line Endings

7.  **Set Line Ending Conversion:**

    ```bash
    git config --global core.autocrlf true
    ```

    This configures Git to automatically handle line endings. Use `true` for Windows (converts LF to CRLF on checkout), `input` for Unix/macOS (converts CRLF to LF on commit), and `false` to disable.

#### Configuring Diff and Merge Tools

8.  **Set Diff Tool:**

    ```bash
    git config --global diff.tool meld
    ```

    This sets the diff tool to `meld`. Replace `meld` with the name of your preferred diff tool.
9.  **Set Merge Tool:**

    ```bash
    git config --global merge.tool vimdiff
    ```

    This sets the merge tool to `vimdiff`. Replace `vimdiff` with your preferred merge tool.

#### Configuring SSH Key

10. **Set SSH Key Path:**

    ```bash
    git config --global core.sshCommand "ssh -i ~/.ssh/your_key"
    ```

    This sets a specific SSH key for Git to use.

#### Configuring Credential Helper

11. **Set Credential Helper:**

    ```bash
    git config --global credential.helper cache
    ```

    This sets Git to cache your credentials in memory for a certain period.

#### Local vs Global vs System Configuration

*   **Local Configuration:** Applies only to the specific repository.

    ```bash
    git config user.name "Repo Specific Name"
    ```
*   **Global Configuration:** Applies to all repositories for the current user.

    ```bash
    git config --global user.name "Global Name"
    ```
*   **System Configuration:** Applies to all users on the system.

    ```bash
    git config --system user.name "System Name"
    ```

#### Removing a Configuration

12. **Unset a Configuration:**

    ```bash
    git config --global --unset user.name
    ```

    This removes the `user.name` configuration.

These commands allow you to effectively manage your Git environment, making sure that all settings are correctly configured for your workflow.
