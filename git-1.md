# git-1

1. **What is Git and why is it used?**
   * **Answer**: Git is a distributed version control system used to track changes in source code during software development. It allows multiple developers to work on a project simultaneously without overwriting each other's changes.
   * **Example**: In a large software project, Git enables version control, ensuring that the codebase is always in a consistent state and that changes can be tracked and managed efficiently.
2. **Explain the difference between `git clone`, `git pull`, and `git fetch`.**
   * **Answer**:
     * `git clone`: Creates a copy of an existing repository.
     * `git pull`: Fetches changes from a remote repository and merges them into the current branch.
     * `git fetch`: Retrieves changes from a remote repository but does not merge them.
   * **Example**: Use `git clone` to initially copy a repository. Use `git pull` to update your local repository with changes from the remote repository and `git fetch` to review changes before merging.
3. **What is a branch in Git?**
   * **Answer**: A branch in Git is a separate line of development. It allows you to work on different features or bug fixes independently.
   * **Example**: Create a new branch for a new feature (`git checkout -b feature-branch`), work on the feature, and then merge it back to the main branch when completed.

**Intermediate Git Questions**

4. **How do you resolve a merge conflict in Git?**
   * **Answer**: When a merge conflict occurs, Git marks the conflict in the files. You need to manually edit the files to resolve the conflict and then add the resolved files to the staging area.
   *   **Example**:

       ```sh
       git merge feature-branch
       # Resolve conflicts in files
       git add resolved-file
       git commit
       ```
5. **Explain the use of `git stash`.**
   * **Answer**: `git stash` temporarily shelves changes you've made to your working directory. This allows you to switch branches or pull in updates without committing your changes.
   *   **Example**:

       ```sh
       git stash
       git checkout other-branch
       git stash pop
       ```
6. **What is the difference between `git reset` and `git revert`?**
   * **Answer**:
     * `git reset`: Moves the current branch pointer to a specific commit, optionally modifying the index and working directory to match.
     * `git revert`: Creates a new commit that undoes the changes from a previous commit.
   * **Example**: Use `git reset` to undo changes in your working directory and index. Use `git revert` to undo a commit without altering the commit history.

**Advanced Git Questions**

7. **How do you use `git rebase` and what are its benefits?**
   * **Answer**: `git rebase` moves or combines a sequence of commits to a new base commit. It is useful for maintaining a clean project history.
   *   **Example**:

       ```sh
       git checkout feature-branch
       git rebase main
       ```

       This re-applies the changes from `feature-branch` onto the latest commit in `main`.
8. **What is the significance of the `.gitignore` file?**
   * **Answer**: The `.gitignore` file specifies intentionally untracked files to ignore. It helps to avoid committing temporary files or build artifacts.
   *   **Example**: A typical `.gitignore` file in a Node.js project might include:

       ```bash
       node_modules/
       .env
       ```
9. **How would you integrate Git with continuous integration/continuous deployment (CI/CD) pipelines?**
   * **Answer**: Integrating Git with CI/CD involves setting up a pipeline that triggers builds and tests automatically on commits or pull requests.
   * **Example**: Use GitHub Actions or Jenkins to set up a pipeline that runs tests on every push to the repository.
10. **Describe the `git bisect` command and its use case.**
    * **Answer**: `git bisect` is used to find the commit that introduced a bug by performing a binary search through the commit history.
    *   **Example**:

        ```sh
        git bisect start
        git bisect bad
        git bisect good COMMIT_HASH
        ```

        Mark commits as good or bad to narrow down the commit that introduced the issue.
