
# Git fundamentals recap

You can find a [git cheatsheet](../../CHEATSHEET-GIT.md) and [CLI cheatsheet](../../CHEATSHEET-CLI.md) with all the commands we work with during this training.

# Exercises: Git fundamentals recap

1. Make sure you are working in the `workspaces/academy-git-fundamentals/exercise-folders` directory. Then create a new folder `git-fundamentals-recap`.

2. Change to your new directory and initiate it with `git init`.

3. Create a `README.md` file with some contents.

**Bonus:** Use the `echo` command to add text to the file!
```
echo "Add some text" >> README.md
```

4. Check the status of the repository using `git status`.

5. Stage the README.md file using `git add README.md`. Check the status of the repository again. What changed?

6. Commit the staged changes with an appropriate commit message. Now we've committed directly to the `main` branch. This can be considered a YOLO branching strategy.

7. Now create a new branch called `new-feature` and switch to it. You can do this in one command using `git checkout -b new-feature`. 

8. Edit the README.md and add a new file `my_python_file.py` with some python code in, for example:
```python
print("Hello, World!")
```

9. Commit the changes to the `new-feature` branch and switch back to the `main` branch. 

10. Merge the `new-feature` branch into the `main` branch.

11. Check the history of the repository using `git log`. Compare this to using ` git log --oneline`.

12. In the `main` branch use `git status` to check your working tree is clean.