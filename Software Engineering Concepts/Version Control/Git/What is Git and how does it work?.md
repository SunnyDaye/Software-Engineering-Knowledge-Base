# What is Git?
Git is a DVCS that functions like a miniature file system with the capability to track and store versions of files in a local database.
# How does it work?
## Snapshots
Git thinks of its data more like a stream of snapshot. Git's data is a set of snapshots of a miniature file system. Every time you commit, or save the state of your project in Git, it basically takes a picture of what all your files look like at that moment and stores a reference to that snapshot. To be efficient, if files have not changed, Git doesn't store the file again, just a link tot he previous identical file it has already stored.
## Keeping things Local
The entire history of the project is stored on your local disk. This mean that whenever git performs an operation, the operation could just pull data from the local database.
### Benefits
- you don't need data from another computer
- you don't need ask a remote server to perform a difference calculation on files
- you don't need to pull an older version of a file from the remote server to perform a difference calculation locally
- most git operations are instantaneous 
- you can work offline until you need to work with remote repos
## Integrity
Everything is Git is check-summed before it is stored and is then referred to by that checksum. Git uses the SHA-1 hash mechanism. This hash is a 40 character string composed of hexadecimal characters(0-9 and a-f) and are calculated based on the contents of a file or directory structure in Git. Git actually stores everything in its database not by filename but by the hash value of its contents.
### Benefits
-  you cannot lose information, change a file, or get file corruption without Git knowing about it
## Generally only adds data
As in most VCSs, you can lose or mess up changes you haven't committed; but after you commit a snapshot into Git, it is very difficult to lose, especially if you regularly push your database to another repository.
## Git and the file system
There are three main states of a file inside of a git repository: modified, staged, and committed. A file is modified when the file has changed but the change is not tracked. A file is staged when the file has been flagged to be included in the next snapshot of the repo. A file is committed when the file's data has been safely stored in git's local database. This implies 3 main sections of a git project.
### The sections of a git project
#### .git directory
The git directory is where Git stores the metadata and object database for your project. The git directory is the most important part of a git project. The git directory is what is copied when you clone a repo.

#### Working directory
The working directory is a single checkout of one version of the project. These files are pulled out of the compressed database in the Git directory and placed on disk for you to use or modify.

#### Staging area
The staging are is a file, generally contained in you git directory, that stores information about what will go into your next commit.
### Git project workflow
1. You checkout a specific version of your git project
2. You modify files in your working directory
3. You stage the files, adding snapshots of them to your staging area
4.  You do a commit, which takes the files as they are in the staging area and stores that snapshot permanently to your Git directory

