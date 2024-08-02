# git-2

* **How do you handle a situation where you need to test a specific commit in the past?**
  * **Answer**: Checkout the specific commit using `git checkout COMMIT_HASH`. After testing, return to the latest commit using `git checkout main` or the appropriate branch.
  *   **Example**:

      ```sh
      git checkout abc1234
      # Perform testing
      git checkout main
      ```
* **What steps would you take if your local branch is significantly behind the remote branch?**
  * **Answer**: First, fetch the latest changes from the remote repository, then rebase or merge them into your local branch.
  *   **Example**:

      ```sh
      git fetch origin
      git rebase origin/main
      ```
