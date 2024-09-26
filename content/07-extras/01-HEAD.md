# What is `HEAD` in git?

`HEAD` in Git points to your current commit, the "latest" commit on your current branch.

It's a pointer that tells you where you are in the commit history.

## Refer to somewhre else in the history

### What does HEAD^ mean?

`HEAD^` refers to the parent of the current `HEAD` commit. In other words... **the commit before the current one**. It's equivalent to saying "one commit before the current commit."

- You can also use `HEAD^^` to go back **two commits**... 
- `HEAD^^^` to go back three
- `HEAD^^^^` for four

and so on...

A more common notation is `HEAD~n` to go back `n` number of commits. For example:

- `HEAD~1`: Equivalent to HEAD^, goes back 1 commit.
- `HEAD~2`: Goes back 2 commits, and so on.