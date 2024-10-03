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

###States

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