### What is a Merge Conflict?

A **merge conflict** happens when Git is unable to automatically reconcile differences between two branches that you're trying to merge. This usually occurs when:
- **Two people edit the same part of a file** on different branches.
- **Conflicting changes** are made to a file, and Git can't decide which changes should be kept.

#### Example Scenario
- You and a collaborator are working on the same file in two separate branches.
- Both of you make changes to the same lines in the file.
- When you try to merge your changes into a shared branch (e.g., `main`), Git encounters conflicting changes and doesn't know which one to apply. It will then notify you of the conflict, leaving the file in a conflicted state that you need to resolve manually.

### How to Resolve a Merge Conflict
1. **Identify the Conflicted Files**: When you try to merge, Git will let you know which files are in conflict.
2. **Open the Conflicted Files**: The conflicting sections will be marked by Git with special markers:
   - `<<<<<<< HEAD`: Indicates the current branch's changes.
   - `=======`: Separates the two conflicting changes.
   - `>>>>>>> <branch>`: Indicates the changes from the branch you're merging in.
3. **Resolve the Conflict**: You have to manually decide which changes to keep:
   - Keep one version of the change.
   - Combine both changes if needed.
   - Delete or edit the conflicting lines.
4. **Mark the Conflict as Resolved**: After editing, stage the file using `git add <file>`.
5. **Complete the Merge**: Commit the resolution using `git commit`.

### Exercise

Simulating a Merge Conflict in Codespaces / VS Code

1. Go to your terminal and make sure you are working in `/workspaces/academy-git-fundamentals/exercise-folders`

2. Create a new directory and initialize a Git repository:
     ```bash
     mkdir merge-conflict
     cd merge-conflict
     git init
     ```

3. Create a file called `pride-and-prejudice.txt` and add the following content, add and commit the file with the commit message `"Initial commit"`.
```
It is a truth universally acknowledged, that a
single man in possession of a good fortune,
must be in want of 
a wife.
```

#### Act as Worker A

4. Create and checkout a new branch called `zombies`

5. Modify the file to say:
```
It is a truth universally acknowledged, that a
zombie in possession of brains,
must be in want of
more brains.
```

6. Add and commit your changes to this branch.

#### Update the main branch

7. Switch Back to the Main Branch

8. Modify the file to say: 
```
It is a falsehood acknowledged in no place, that a
married woman in possession of small
hardship
must be in want of
singlehood. 
```

9. Add and commit this change to the main branch.

#### Trigger the conflict

10. Merge the Branch and Trigger a Conflict
     ```bash
     git merge zombies
     ```

You should see a **merge conflict** message. 
```
error: Merging is not possible because you have unmerged files.
hint: Fix them up in the work tree, and then use 'git add/rm <file>'
hint: as appropriate to mark resolution and make a commit.
fatal: Exiting because of an unresolved conflict.
```

11. Open the file `pride-and-prejudice.txt` by either **manually editing the file** or by selecting one of the accept buttons.
```text
<<<<<<< HEAD
=======
>>>>>>> zombies
```

12. Add and commit the file in the terminal using `git add` and `git commit` with a message that states it's fixing the merge conflict.

13. In the `main` branch use `git status` to check your working tree is clean. Add and commit any changes with the commit message `"End of merge conflict exercises"

### Summary
- **Why Merge Conflicts Happen**: They occur when two branches have conflicting changes that Git can't automatically reconcile.
- **How to Resolve Them**: Open the conflicted file, manually resolve the differences, stage the file, and commit the changes.

A lot of tools, like VS Code, have ways of working through things like merge conflicts to make it easier to reconcile changes.