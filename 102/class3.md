1. **What is version control?** 
Version Control is a system that allows you to revisit various versions of a file or set of files by recording changes. Through version control, one can revert a file or project to a previous version, track modifications and modifying individuals, and compare changes. By utilizing a Version Control System (VCS), mistakes with files can easily be rectified.

2. **What is cloning in Git?** 
In Git, cloning is the process of copying a remote repository to your local machine. It gives you a full copy of the project, including all files, commits, and branches, so you can work on it locally.

*Reasons to clone*
-you get a full copy
-work offline
-sync easily

example: 'git clone https://github.com/username/repository.git'

**What is Git?**
*Snapshots*

Git is a DVCS that stores data in a file system made up of snapshots. Each time you save a changed version of your project — called commit — Git creates a snapshot of the file and stores a reference to it. If the file has not changed, Git only stores a reference to the already-stored identical version of it.

*Local Operations*

Git mostly relies on local operations because most necessary information can be found in local resources. This allows for process expediency because a project’s history resides on the local disk, eliminating the need to fetch history information from the server, and allowing one to continue work on a project even when not online or on a VPN.

*Tracking Changes*

Every single change applied to any file or directory is tracked by Git. And, as the gatekeeper, Git will always detect file corruption or loss of information in transit.

*Loss of Data*

Git is set up to greatly minimize the possibility of irreversible damage to files, such as accidentally lost data. Git makes it extremely difficult for a snapshot of your file that is committed to be lost.

### States

Files in Git can reside in three main states: committed, modified and staged.

*Committed*

Data is securely stored in a local database

*Modified*

File has been changed but not committed to the database

3. **What is the command to track and stage files?**
**answer**:
'git add' or 'git add .'

4. **What is the command to take a snapshot of your changed files?**
**answer**: 'git commit' -m "Fixed bug in feature X"

5. **What is the command to send your changed files to Github?**
**answer**: 'git push origin main'

**_Notes_**
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

**Follow these steps:**
1. Git status

2. Git add . (the dot means 'all')

3. Git commit (must add a comment using -m"comment here")

4. Git push origins main (this will push the update)