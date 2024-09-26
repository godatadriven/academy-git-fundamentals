# Remote Repositories

Remote repositories allow you to share your code with others and synchronize changes between multiple developers. They are Git repositories hosted on a remote server, usually on a code hosting platform like GitHub, GitLab, or Bitbucket.

<img src="../images/git-remote.png" alt="" style="width: 400px;"/>

## Adding a Remote Repository

To add a remote repository to your local Git repository, use the `git remote add` command followed by a name (usually "`origin`" for the main remote) and the repository URL:

```bash
git remote add origin https://github.com/user/repo.git
```

## Listing Remote Repositories

To list all remote repositories connected to your local Git repository, we can use:

```bash
git remote -v
```
