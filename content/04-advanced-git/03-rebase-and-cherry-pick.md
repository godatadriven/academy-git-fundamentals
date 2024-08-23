
# Rebasing and Cherry-picking

In this section, we will discuss two advanced Git techniques: rebasing and cherry-picking. These techniques allow you to manipulate your commit history and selectively apply changes from one branch to another.

![](../images/rebase.png)

## Rebasing

Rebasing is the process of reapplying commits on top of another branch or commit. It helps maintain a linear project history and avoids unnecessary merge commits.

To rebase your current branch's commits onto a base branch, use the following command:

```bash
git rebase <base_branch>
```

If there are any conflicts, resolve them and then proceed with the rebase using:

```bash
git rebase --continue
```

Be cautious when rebasing published commits, as it can cause confusion and conflicts for collaborators.

A great visualization of rebasing can be found [in this video](https://www.youtube.com/watch?v=0chZFIZLR_0) (and many other places).

## Cherry-picking

Cherry-picking allows you to selectively apply specific commits from one branch to another. This is useful when you need specific changes from another branch without merging the entire branch.

To apply a desired commit to your current branch, use the following command:

```bash
git cherry-pick <commit_hash>
```

If there are any conflicts, resolve them and then proceed with the cherry-pick using:

```bash
git cherry-pick --continue
```

Both rebasing and cherry-picking maintain the original commit authorship and date information. In both cases, however, the commit hash changes.


## Exercises

1. Navigate outside of the `academy-shell-and-git` directory using `cd ..` a few times (or `cd ~`). Then create a new folder `new-repository` and initiate it with `git init`. Then add and commit some file(s) to it.

2. Create a new branch `new-feature` and switch to it. Then add and commit some changes to this branch. Run `git log --oneline --graph --all` to see the commit history.

3. Switch back to the `main` branch and create a new commit. Make sure it doesn't conflict with the `new-feature` branch. Check the commit history again.

4. Switch back to the `new-feature` branch and rebase it onto the `main` branch. 

5. Check the commit history again. What changed?

6. Create another branch `another-feature` and switch to it. Then add and commit some changes to this branch (make sure it doesn't conflict with the other branches). Check the commit history.

7. Switch back to the `my-feature` branch and cherry-pick a commit from the `another-feature` branch. Check the commit history again. What changed?
