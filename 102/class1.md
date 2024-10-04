# **Command line**

A **command line**, or terminal, is a text based interface to the system. You are able to enter commands by typing them on the keyboard and feedback will be given to you similarly as text.
The command line typically presents you with a prompt. As you type, it will be displayed after the prompt. Most of the time you will be issuing commands.

Here are some of the most commonly used Git commands in the terminal, grouped by purpose:
1. *Basic Setup*
git config --global user.name "Your Name"
Sets the user name for commits.
git config --global user.email "your_email@example.com"
Sets the email for commits.
2. *Starting a Project*
git init
Initializes a new Git repository.
git clone <repository-url>
Clones an existing Git repository from a URL.
3. *Basic Workflow*
git status
Displays the state of the working directory and staging area.
git add <file>
Stages a file for the next commit.
git add .
Stages all files (new, modified, and deleted) for the next commit.
git commit -m "commit message"
Commits the staged changes with a message.
git commit --amend
Modifies the most recent commit (e.g., to edit the commit message or include additional changes).
4. *Branching and Merging*
git branch
Lists all branches in the repository.
git branch <branch-name>
Creates a new branch.
git checkout <branch-name>
Switches to the specified branch.
git checkout -b <branch-name>
Creates and switches to a new branch.
git merge <branch-name>
Merges the specified branch into the current branch.
5. *Remote Repositories*
git remote -v
Shows the remote URLs for the repository.
git push
Pushes changes from the local repository to the remote repository.
git push origin <branch-name>
Pushes a specific branch to the remote repository.
git pull
Fetches and integrates changes from the remote repository to the current branch.
git fetch
Fetches changes from the remote repository but does not merge them.
6. *Viewing and Inspecting*
git log
Displays the commit history.
git log --oneline
Shows a simplified commit history in a single line.
git diff
Shows changes between working directory and the index or between commits.
git show <commit>
Displays details of a specific commit.
7. *Stashing Changes*
git stash
Temporarily saves changes without committing them.
git stash apply
Re-applies stashed changes.
git stash pop
Re-applies and removes the stashed changes from the list.
8. *Undoing Changes*
git reset <file>
Unstages a file without changing the working directory.
git reset --hard
Resets the index and working directory to the last commit (careful: discards changes).
git revert <commit>
Reverts a specific commit by creating a new commit.
9. *Deleting Branches*
git branch -d <branch-name>
Deletes a local branch (if it has been merged).
git branch -D <branch-name>
Force deletes a local branch (even if it hasn’t been merged).
10. *Tagging*
git tag <tag-name>
Creates a tag for a specific commit.
git push origin <tag-name>
Pushes a specific tag to the remote repository.
These commands form the core of most Git workflows.



