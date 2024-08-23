# Checking Differences Between Commits

In this section, we will explore how to check the differences between commits.

## Viewing Changes Between the Working Directory and the Staging Area

To view the changes between your working directory and the staging area, use the following command:
```bash
git diff
```

This will show you the differences between your working directory and the staged changes.

## Viewing Changes Between the Staging Area and the Latest Commit

To view the changes between the staging area and the latest commit, use the following command:

```bash
git diff --staged
```

This will show you the differences between the staged changes and the latest commit.

## Viewing Changes Between Different Commits

To view the changes between two different commits, use the following command:

```bash
git diff <commit1> <commit2>
```

Replace `<commit1>` and `<commit2>` with the commit hashes or references you want to compare.
