# git-4

To revert a recent Git commit, you have a few options depending on your needs:

#### 1. **Undo the Last Commit (but keep the changes):**

If you want to undo the last commit but keep the changes in your working directory (so you can re-commit them), use:

```bash
git reset --soft HEAD~1
```

This command moves the `HEAD` pointer back to the previous commit but leaves your changes staged.

#### 2. **Undo the Last Commit (and discard the changes):**

If you want to undo the last commit and discard all changes:

```bash
git reset --hard HEAD~1
```

This command moves the `HEAD` pointer back to the previous commit and discards all changes in the working directory.

#### 3. **Revert the Last Commit (keep history intact):**

If you want to create a new commit that reverts the changes made in the last commit (while keeping the history intact):

```bash
git revert HEAD
```

This will create a new commit that undoes the changes introduced by the last commit.

#### 4. **Undo a Pushed Commit:**

If you’ve already pushed the commit and want to undo it, you can use:

*   For **reset** (only if you are sure and working in a shared repo):

    ```bash
    git reset --hard HEAD~1
    git push -f
    ```

    This rewrites history and should be used with caution, especially in shared repositories.
*   For **revert** (safest for shared repositories):

    ```bash
    git revert HEAD
    git push
    ```

    This adds a new commit that reverts the changes.

#### 5. **Undo Multiple Commits:**

If you need to undo more than one commit, you can adjust the `HEAD~1` to `HEAD~n`, where `n` is the number of commits you want to undo:

```bash
git reset --soft HEAD~3  # Undo the last 3 commits, keep changes
git reset --hard HEAD~3  # Undo the last 3 commits, discard changes
git revert HEAD~3..HEAD  # Revert the last 3 commits
```

Choose the method that best suits your situation.
