# Pull and Push Changes

In this section, we'll cover the essential Git commands for syncing your local repository with a remote repository.

<img src="../images/git-remote.png" alt="" style="width: 400px;"/>

## Fetching Changes from a Remote Repository (`git fetch`)

`git fetch` retrieves changes from the remote repository, but does not merge them. This allows you to review the changes before integrating them into your local branch.

## Merging Fetched Changes (`git merge`)

Once you have fetched changes, use `git merge` to integrate them into your local branch. Replace `<branch>` with the appropriate branch name.
    
```bash
git merge origin/<branch>
```

## Pulling Changes from a Remote Repository (`git pull`)

`git pull` is a combination of `git fetch` and `git merge`. It fetches changes from the remote repository and automatically merges them into your local branch.
```bash
git pull origin <branch>
```

## Pushing Changes to a Remote Repository (`git push`)

`git push` uploads your local changes to the remote repository. Make sure your local branch is up-to-date with the remote branch before pushing.

```bash
git push origin <branch>
```
