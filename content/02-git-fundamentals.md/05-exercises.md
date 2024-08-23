
# Exercises: Git fundamentals

1. Navigate outside of the `academy-shell-and-git` directory using `cd ..` a few times (or `cd ~`). Then create a new folder `new-repository` and initiate it with `git init`.

2. Create a README.md file with some contents using the `echo` command, or using a text editor (e.g. `vi` or `nano`). Check the status of the repository using `git status`.

3. Stage the README.md file using `git add README.md`. Check the status of the repository again. What changed?

4. Commit the staged changes with an appropriate commit message. Now we've committed directly to the `main` branch. This can be considered a YOLO branching strategy.

5. Let's now create a new branch called `new-feature` and switch to it. You can do this in one command using `git checkout -b new-feature`. Now change some files, or create some new ones.

6. Add your changes to the staging area and check the difference between the staging area and the last commit using `git diff --staged`. What changed?

7. Commit the changes to the `new-feature` branch and switch back to the `main` branch. 

8. Merge the `new-feature` branch into the `main` branch.

9. Check the history of the repository using `git log`. And try to visualize the graph using:
```bash
git log --decorate --graph --pretty=oneline --abbrev-commit --color --all
```
