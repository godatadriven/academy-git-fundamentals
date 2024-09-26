# Status and log

In this section, we'll cover how to check the status of your repository and view the commit history using `git status` and `git log`.

## Checking the status of your repository (`git status`)

`git status` shows the current state of your working directory, including any changes made since the last commit. It displays untracked files, modified files, and staged changes.

```bash
git status
```

## Viewing the commit history (`git log`)

`git log` displays the commit history of your repository, showing the most recent commits first. It includes the commit hash, author, date, and commit message.

```bash
git log
```

## Filtering and formatting the commit history (`git log` options)

You can customize the output of `git log` using various options. For example, you can limit the number of commits displayed, filter by author, or format the output.

```bash
git log --oneline
git log -n 5
git log --author="John Doe"
git log --pretty=format:"%h - %an, %ar : %s"
```

These commands display a one-line summary, limit the output to the last 5 commits, filter by author, and customize the output format, respectively.

You can even print the commit history as a graph using the `--graph` option and some additional options to make the output more readable:

```bash
git log --decorate --graph --pretty=oneline --abbrev-commit --color --all
```
