
# Advanced Git: Interactive Add, Commit, and Rebase

In this short guide, we will cover the essentials of interactive add, commit, and rebase in Git. These features help you create focused, well-organized commits and clean up your commit history.

## Interactive Add

Interactive add allows you to selectively stage changes using the `git add -p` command. This is useful for organizing related changes together and reviewing changes before staging them. To use interactive add, follow these steps:

1. Run `git add -p`.
2. Review the changes presented and decide whether to stage them or not.
3. Repeat until all desired changes have been staged.

## Interactive Commit

Interactive commit lets you choose specific changes to include in a commit using `git commit --interactive`. This feature helps you review, stage, and unstage changes in an interactive menu. To use interactive commit, follow these steps:

1. Run `git commit --interactive`.
2. Review the changes presented in the interactive menu.
3. Choose the changes you want to include in the commit.
4. Complete the commit with a descriptive message.

## Interactive Rebase

Interactive rebase allows you to modify your commit history using the `git rebase -i` command. With interactive rebase, you can combine, edit, reorder, or delete commits interactively. This is useful for cleaning up your commit history before merging or sharing changes. To use interactive rebase, follow these steps:

1. Run `git rebase -i` followed by the commit hash or reference you want to rebase onto.
2. Review the list of commits presented in your text editor.
3. Modify the list by changing the commands (e.g., pick, edit, squash, drop) in front of each commit.
4. Save and close the file to start the interactive rebase process.
5. Follow the on-screen instructions to complete the rebase.

## Exercises

1. In your `new-repository`, make sure you have two existing files committed.

2. Now make changes to those two files, without committing. Use interactive add to stage only one of the files.

3. Use interactive commit to commit the staged changes.
