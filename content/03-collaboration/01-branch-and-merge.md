
# Branching and Merging

Branches allow you to work on different features or bug fixes in isolation and later combine them into a single, stable codebase.

<img src="../images/branch.png" alt="" style="width: 500px;"/>

## Creating and Switching Branches

To create a new branch, use the `git branch` command followed by the branch name:

```bash
git branch new-feature
```

To switch to the newly created branch, use the `git checkout` command:

```bash
git checkout new-feature
```

You can also create and switch to a new branch in one command using the `-b` flag:
```bash
git checkout -b new-feature
```

## Merging Branches

To merge changes from one branch into another, first, switch to the target branch:

```bash
git checkout main
```

Then, use the `git merge` command followed by the branch you want to merge:

```bash
git merge new-feature
```

This will combine the changes from the `new-feature` branch into the main branch.

## Resolving Merge Conflicts

Sometimes, Git cannot automatically merge changes due to conflicting modifications in the same file. In this case, you need to manually resolve the conflicts.

Open the conflicting file in a text editor and look for conflict markers (`<<<<<<<`, `=======`, and `>>>>>>>`). Edit the file to resolve the conflicts, keeping the desired changes and removing the conflict markers.

After resolving the conflicts, stage the changes:

```bash
git add conflicting-file.txt
```

Finally, commit the merged changes:

```bash
git commit -m "Resolve merge conflicts"
```
