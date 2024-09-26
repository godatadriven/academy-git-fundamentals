### Git Fundamentals Cheat Sheet


| **Command**                       | **Description**                                                  | **Example**                                    |
|-----------------------------------|------------------------------------------------------------------|------------------------------------------------|
| `git init`                        | Initialize a new Git repository                                  | `git init`                                     |
| `git status`                      | Check the status of files (tracked, untracked, staged)           | `git status`                                   |
| `git add <file>`                  | Stage a specific file                                            | `git add file.txt`                             |
| `git add .`                       | Stage all changes                                                | `git add .`                                    |
| `git commit -m "<message>"`       | Commit staged changes with a message                             | `git commit -m "Initial commit"`               |
| `git push origin <branch>`        | Push commits to the remote repository                            | `git push origin main`                         |
| `git pull origin <branch>`        | Fetch and merge changes from the remote repository               | `git pull origin main`                         |
| `git fetch`                       | Fetch changes from the remote without merging                    | `git fetch`                                    |
| `git diff`                        | Show unstaged changes in the working directory                   | `git diff`                                     |
| `git diff --staged`               | Show changes staged for the next commit                          | `git diff --staged`                            |
| `git log`                         | View the commit history                                          | `git log`                                      |
| `git log --oneline `              | View the commit history in a one-line format                     | `git log --oneline --graph --all`              |
| `git log --oneline --graph --all` | View the commit history in a graph format                        | `git log --oneline --graph --all`              |
| `git merge <branch>`              | Merge the specified branch into your current branch              | `git merge new-feature`                        |
| `git remote -v`                   | View the remote repository URL(s)                                | `git remote -v`                                |
| `git branch`                      | List all branches                                                | `git branch`                                   |
| `git diff <branch-name>`          | Compare your current branch with another branch                  | `git diff main`                                |
| `git reset <file>`                | Unstage a file but keep changes                                  | `git reset file.txt`                           |
| `git branch -d <branch>`          | Delete a local branch                                            | `git branch -d old-feature`                    |
| `git checkout <branch>`           | Switch to an existing branch                                     | `git checkout new-feature`                     |
| `git checkout -b <branch>`        | Create and switch to a new branch                                | `git checkout -b new-feature`                  |
| `git rebase <branch>`             | Reapply your commits on top of another branch                    | `git rebase main`                              |
| `git cherry-pick <commit-hash>`   | Apply a specific commit to your current branch                   | `git cherry-pick 4f4a34d`                      |
| `git push -u origin <branch>`     | Push a new branch to the remote repository                       | `git push -u origin new-feature`               |

