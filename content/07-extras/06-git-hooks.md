# Git Hooks

Git hooks are custom scripts that run automatically during specific Git events, such as committing or pushing changes. They help enforce policies, automate tasks, and improve workflow within a project.

## Hooks Directory

Hooks are stored in the `.git/hooks` directory of a Git repository and can be written in any scripting language (e.g., Bash, Python).

## Common Use Cases

1. Checking for code style and formatting before committing (`pre-commit` hook).
2. Validating commit messages (`commit-msg` hook).
3. Running tests or other build tasks before pushing (`pre-push` hook).

## Creating a Hook

To create a hook, simply name the script file after the desired hook event (e.g., `pre-commit`) and make it executable (`chmod +x pre-commit`).

## Sharing Hooks

Hooks are not versioned by default, but you can share them across a team by storing them in a separate directory and configuring Git to use that directory for hooks.

## Exercises

1. Create a `pre-commit` hook that prints a motivational message every time you commit changes.

2. Change the `pre-commit` hook so it prints the ratio of vowels vs anti-vowels in the commit message, or in the file changes.
