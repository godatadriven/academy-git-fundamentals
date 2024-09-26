# Working with Submodules

Submodules allow you to include other repositories within your repository, making it easier to manage dependencies and share code between projects.

## Adding a Submodule

To add a submodule to your repository, use the following command:

```bash
git submodule add <repository-url> <path>
```

This will clone the specified repository into the path provided.

## Cloning a Repository with Submodules

When cloning a repository that contains submodules, use the `--recurse-submodules` flag to ensure that the submodules are also cloned:

```bash
git clone --recurse-submodules <repository-url>
```

## Updating Submodules

To update the submodules to their latest commit, use the following command:

```bash
git submodule update --remote --merge
```

This will fetch the latest changes from the submodule's remote repository and merge them into your submodule.

## Removing a Submodule

To remove a submodule from your repository, first remove the submodule entry in the `.gitmodules` file and the `.git/config` file. Then, use the following command to remove the submodule from your project:
```bash
git rm --cached <path>
```

Finally, commit the changes to complete the removal process.
