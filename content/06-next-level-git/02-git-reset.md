# Unstaging and Undoing commits

`git reset` is a powerful command that allows you to undo changes in your working directory and staging area. It comes in handy when you need to:

- Unstage files after staging them.
- Revert to a previous commit, either keeping or discarding changes.

## Unstaging files

Let's say you are working late at night on a project, you are about to log off, but not before commiting your changes.

You do `git add .` because you don't want to list all the files you changed, but you realise you have some files you don't want commited!

```git
On branch main

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   file1.txt
        new file:   file2.txt
        new file:   lucys_secrets.txt
```

You can reset the file in the same way as using `git add`:

```
git reset lucys_secrets.txt
git commit -m "Only add the non-secret files"
```

## Reverting to a previous commit

Let's say you realized that you also didn't want to include file2.txt, but too late! You've already commited the change!

You can use the following command to undo a commit:
```git reset --soft HEAD^```

You may be wondering.. 
- [What does `HEAD^` mean here?](../07-extras/01-HEAD.md)
- So there's a soft reset, can I also do a [hard reset](../07-extras/02-hard-reset.md)?

## Exercise:

### Exercise: Understanding `git reset` and `git reset --soft`

This exercise will guide you through creating a Git repository, adding files, committing changes, and experimenting with `git reset` and `git reset --soft` to see how they behave.

#### Step-by-Step Instructions

1. Go to your terminal and make sure you are working in `/workspaces/academy-git-fundamentals/exercise-folders`

2. Create a new directory and initialize a git repository:
     ```bash
     mkdir reset-exercise
     cd reset-exercise
     git init
     ```

2. Create two new files, `file1.txt` and `file2.txt`

3. Stage and Commit the Files in one commit

4. Modify `file1.txt` and commit your change.

5. Use the command `git log --oneline` to see the commits that have happened.

5. Use `git reset --soft HEAD^` to Undo the Last Commit

5. Use the command `git log --oneline` to see the commits that have happened.

5. Check the status of your branch, is the modified file in your staging?

6. Use `git reset file1.txt` to unstage the Changes

7. Check your log and status to check what you have done

8. In the `main` branch use `git status` to check your working tree is clean. 


## Exercise 2
### Experiment with `git reset --hard` (Optional)

<font color=maroon>**⚠️Warning:**</font> This will permanently delete uncommitted changes!

1. Add a new file: `important_file.txt` 

2. Commit *only* the important file to the branch

3. Use git status to check that the `file1.txt` is still unstaged

1. Use `git log --onefile` to check the commit history

3. Use `git reset --hard HEAD^` to completely undo all changes in both the working directory and the staging area

1. Use `git log --onefile` to check the commit history

3. Use git status to check there are no staged files

1. In the `main` branch use `git status` to check your working tree is clean. Add and commit any changes with the commit message `"End of git reset exercises"
