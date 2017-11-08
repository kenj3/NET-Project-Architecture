# Git General help & Quick Reference 
This is a general help for using Git and provide a quick reference of all Git comments.

## Download
[Click here to download Git for windows][ref01]

## Document
[Official document][ref02]

## Quick Reference
### Setup and Config
Command | Description
------- | -----------
*git help* | Display help information about Git
*git config* | Display help information about 'git config' command
*git config --list* | Display current configuration
*git config --global user.name "usename"* | Set global username
*git config --global user.email "email"* | Set global email
*git config --local user.name "usename"* | Set local username
*git config --local user.email "email"* | Set local email

### Getting and Create Projects
Command | Description
------- | -----------
*init*  | Create an empty Git repository or reinitialize an existing one
*clone* | Clone a repository into a new directory

### Basic Snapshotting
Command | Description
------- | -----------
*add*   | Add file contents to the index
*status*| Show the current working tree status
*diff*  | Show changes between commits, commit and working tree, etc.
*commit*| Record changes to the repository
*reset* | Reset current HEAD to the specified state

### Branching and Merging
Command   | Description
--------- | -----------
*branch*  | Create a new branch from master
*checkout*| Switch branches or restore working tree files
*merge*   | Incorporate changes from one branch into another 
*log*     | Show commit los

### Sharing and Updating Projects
Command | Description
------- | -----------
*fetch* | Download objects and refs from another repository
*pull*  | Fetch from remote 'master' branch
*push*  | Update remote refs along with associated objects
*remote*| Manage set of tracked repositories

### Inspection and Comparison
Command | Description
------- | -----------
*show*  | Show various types of objects
*log*   | Show commit log
*diff*  | Show changes between commits, commit and working tree.


### Standard Routines
#### Commit your work to server
1. `git add -A` // add all updated files to local stage.
2. `git commit -m "your description"` // commit all added files to local stage.
3. `git push` 


#### Merge changes from a branch to master
1. `git checkout master`         // back to master branch
2. `git merge branch_1_name`     // incorporate branch_1_name into master
3. `git branch -d branch_1_name` // delete branch branch_1_name


[ref01]: https://git-for-windows.github.io/  "Git Download for windows"
[ref02]: https://git-scm.com/docs "Git official document"