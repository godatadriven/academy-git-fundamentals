
# Stashing and Cleaning

In this section, we will cover two useful techniques for managing your working directory: stashing and cleaning. Stashing allows you to temporarily save changes that you do not want to commit yet, while cleaning helps you remove untracked files and directories.

## Stashing

Stashing is useful when you need to switch branches or tasks without committing your current changes. Here are some essential commands for working with stashes:

- `git stash save "message"`: Create a new stash with an optional message.
- `git stash list`: View all stashes.
- `git stash apply`: Apply the latest stash to the working directory.
- `git stash apply stash@{n}`: Apply a specific stash (n is the stash index).
- `git stash drop`: Remove the latest stash.
- `git stash drop stash@{n}`: Remove a specific stash.
- `git stash pop`: Apply and remove the latest stash.
- `git stash branch branch_name`: Create a new branch and apply a stash.

## Cleaning

Cleaning is useful for removing untracked files and directories, such as generated files, build artifacts, and temporary files. Here are some essential commands for cleaning your working directory:

- `git clean -n`: Preview the files that will be removed (dry run).
- `git clean -f`: Force removal of untracked files.
- `git clean -fd`: Remove untracked files and directories.
- `git clean -fX`: Remove only ignored files.
- `git clean -fx`: Remove all untracked and ignored files

## Exercises

1. In your `new-repository`, create some changes in a branch `new-feature` without committing them. Stash them instead, and switch to the `main` branch.

2. Now, switch back to the `new-feature` branch and apply the stash. Then commit the changes.

3. Create some untracked files and directories in your `new-repository`. Then, clean your working directory using the appropriate commands.
