
# Reverting changes

## Undoing Uncommitted Changes

To undo changes to a file that have not been committed yet, use the following command:

```bash
git checkout -- <file>
```

This will restore the file to the state it was in at the last commit.

## Undoing Committed Changes

To undo changes to a file that have already been committed, use the following command:

```bash
git revert <commit_hash>
```

This will create a new commit that reverts the changes introduced by the specified commit.

## Resetting the Working Directory

To reset the working directory to the last commit, use the following command:

```bash
git reset --hard
```

This will discard all uncommitted changes and restore the working directory to the state it was in at the last commit.

## Resetting the Staging Area

To reset the staging area to the last commit, use the following command:

```bash
git reset
```

This will unstage all staged changes and restore the staging area to the state it was in at the last commit.

## Reset to a Specific Commit

To reset the working directory and staging area to a specific commit, use the following command:

```bash
git reset --hard <commit_hash>
```

This is useful for discarding all changes since a specific commit, and starting over from that commit.

**Note**: Don't do reset on remote branches, unless you know what you're doing.
