Here are the steps to squash commits in Git, followed by an exercise to help you practice it.

### Steps to Squash Commits in Git

1. **Ensure your branch is up-to-date**  
   Before squashing, make sure your branch is up-to-date with the latest changes:
   ```bash
   git fetch origin
   git pull origin <branch>
   ```

2. **Identify the commits you want to squash**  
   Decide how many commits you want to combine. For example, if you want to squash the last 3 commits, you’ll use `git rebase -i` and specify the number of commits:
   ```bash
   git rebase -i HEAD~3
   ```

3. **Mark commits for squashing**  
   This command opens your text editor with a list of commits. Each commit will be prefixed by the word `pick`. To squash a commit, replace `pick` with `squash` (or simply `s`), keeping `pick` for the first commit in the list. The other commits will be squashed into the first one.

4. **Edit the commit message**  
   After squashing, Git will prompt you to edit the combined commit message. Modify or combine the commit messages as necessary, then save and close the editor.

5. **Complete the rebase**  
   After editing the commit message, Git will complete the rebase and squash the commits into one.

6. **Push the squashed commit to the remote repository**  
   If the branch has already been pushed to a remote, you’ll need to force-push the changes because you have rewritten the commit history:
   ```bash
   git push origin <branch> --force
   ```

### Exercise to Practice Squashing Commits

#### Objective:  
You will make three separate commits and then squash them into one.

#### Steps:
1. **Create a new directory and initialize a Git repository**  
   ```bash
   mkdir squashing-commits
   cd squashing-commits
   git init
   ```

2. **Create and commit files**
   - Add a base file called `base.md` and commit the file with `"Initial commit"
   - Create a new file called `file1.txt` and add some text to it. Commit the file with a new commit message `"Add file 1`"`
   - Create a second file `file2.txt` and commit it with a new commit message `"Add file 2`"`
   - Modify `file1.txt` by adding text to it, then commit again:
     ```bash
     echo "Append text to file1.txt" >> file1.txt
     git add file1.txt
     git commit -m "Modify file 1"
     ```

3. **Check your commit history**  
   Verify that there are four commits (including Innitial commit and the most recent being HEAD):
   ```bash
   git log --oneline
   ```

4. **Squash the last two commits into the first commit**  
   Use interactive rebase to squash the last two commits:
   ```bash
   git rebase -i HEAD~3
   ```

5. **Follow the squashing process**  
   - The rebase editor file should now have opened.
   - In the editor, keep `pick` for the first commit and change the other two commits from `pick` to `squash`.
   - Close the file.

6. **Update the commit message**
   - The commit message editor file should now have opened.
   - Edit the first commit message to what ever you like.

7. **Verify your commits**  
   After the rebase, verify that there is only one commit:
   ```bash
   git log --oneline
   ```

8. In the `main` branch use `git status` to check your working tree is clean.