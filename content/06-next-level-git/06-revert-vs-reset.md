### Difference Between `git reset` and `git revert`

Both `git reset` and `git revert` are used to undo changes in Git, but they work in different ways and are used for different scenarios:

#### **`git reset`**
- **Changes Commit History**: It moves the `HEAD` pointer back to a previous commit, erasing commits that come after it in your branch.
- **Use Case**: Best for local, private work when you want to undo changes and rewrite the history.
- **Effect on Commits**: The commits you "reset" to are removed from the history.
- **Effect on Working Directory**: Depending on the reset mode (`--soft`, `--mixed`, or `--hard`), it can unstage changes or completely remove changes from your working directory.
  - `--soft`: Keeps all changes staged.
  - `--mixed` (default): Unstages changes but keeps them in the working directory.
  - `--hard`: Discards all changes in the working directory and staging area.

#### **`git revert`**
- **Does Not Change Commit History**: Instead of removing or rewriting commits, it creates a **new commit** that undoes the changes made in a specific commit.
- **Use Case**: Best for public or shared repositories when you want to undo a specific change but preserve the commit history.
- **Effect on Commits**: A new commit is created that undoes the changes from a previous commit.
- **Effect on Working Directory**: Does not modify your working directory unless there are merge conflicts during the revert.

### Summary:
- **`git reset`**: Rewrites history by moving the `HEAD` pointer, potentially removing commits.
- **`git revert`**: Safely undoes a commit by creating a new commit that reverses changes without modifying history.

---

### Exercise: Exploring `git reset` and `git revert`

This exercise will guide you through using both `git reset` and `git revert` so you can see the differences.

##### 1. **Set Up the folder**
-  Go to your terminal and make sure you are working in `/workspaces/academy-git-fundamentals/exercise-folders`
- Create a new folder and initialize it as a git repository
  ```bash
  mkdir reset-revert
  cd reset-revert
  git init
  ```

##### 2. **Create and Commit Files**
- Create a file called `file1.txt` and add some content:
  ```bash
  echo "Initial content for file1" > file1.txt
  ```
- Stage and commit the file:
  ```bash
  git add file1.txt
  git commit -m "Initial commit with file1"
  ```

##### 3. **Modify the File and Commit the Changes**
- Make a modification to `file1.txt`:
  ```bash
  echo "Additional content in file1" >> file1.txt
  ```
- Stage and commit the change:
  ```bash
  git add file1.txt
  git commit -m "Added more content to file1"
  ```

##### 4. **Use `git reset` to Undo the Last Commit**
- Run the following command:
  ```bash
  git reset --soft HEAD^
  ```
- **Check the result**:
  - Run `git status`: You’ll see that the changes are still staged, but the last commit is undone.
  - Run `git log`: You’ll notice the last commit is removed from the commit history.

##### 5. **Commit Again for the Revert Test**
- Recommit the changes to bring them back into history:
  ```bash
  git commit -m "Added more content to file1"
  ```

##### 6. **Use `git revert` to Undo the Last Commit**
- Run the following command:
  ```bash
  git revert HEAD
  ```
- **Resolve any conflicts if prompted**. If no conflict occurs, Git automatically generates a commit that undoes the changes from the last commit.

##### 7. **Check the Result**
- **View the log**:
  ```bash
  git log --oneline
  ```
  - You'll see a new commit message like **"Revert 'Added more content to file1'"**, which undoes the last commit without altering the commit history.
- **Check the file**: The content added in the last commit will be removed from `file1.txt`.

### Key Takeaways:
- **`git reset --soft HEAD^`** removes the last commit but keeps the changes staged.
- **`git revert HEAD`** creates a new commit that undoes the changes in the last commit without deleting any history.