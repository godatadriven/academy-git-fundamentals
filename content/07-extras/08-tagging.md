# Git Tagging

Git tags are used to mark specific points in a repository's history, often for marking release points. There are two types of tags: lightweight and annotated.

## Git Tags: Lightweight and Annotated

- Lightweight tags: simple pointers to a commit, created with `git tag <tag_name>`.
- Annotated tags: store additional metadata, like tagger name, email, and date, created with `git tag -a <tag_name> -m "message"`.

## Listing and Searching Tags

- List all tags: `git tag`
- Search for tags with a specific pattern: `git tag -l "v1.*"`

## Checking Out and Comparing Tags

- Checkout a tag: `git checkout <tag_name>`
- Compare two tags: `git diff <tag_name1> <tag_name2>`

## Tagging Previous Commits

- Tag a specific commit: `git tag -a <tag_name> <commit_hash>`

## Pushing and Pulling Tags

- Push a single tag to a remote repository: `git push origin <tag_name>`
- Push all tags to a remote repository: `git push origin --tags`
- Fetch tags from a remote repository: `git fetch --tags`

## Deleting Tags

- Delete a local tag: `git tag -d <tag_name>`

## Exercises

1. Tag the most recent commit in your repository.

2. Checkout to a different branch and create a new commit and also give it a tag.

3. Compare the most recent commit with the tagged commit, without using git hashes.
