Git Commands 
============
___

<p align="center">
<b><b><i> -_A list of my commonly used Git (distributed version control system) commands_- </i></b>
</p>


### Getting & Creating Projects

| Command | Description |
| ------- | ----------- |
| `pwd` | Current Working Directory |
| `git init` | Initialize a local Git repository |
| `git clone ssh://git@github.com/[username]/[repository-name].git` | Create a local copy of a remote repository |

### Basic Snapshotting

| Command | Description |
| ------- | ----------- |
| `git status` | Check status |
| `git add [file-name.txt]` | Add a file to the staging area |
| `git add -A` | Add all new and changed files to the staging area |
| `git commit -m "[commit message]"` | Commit changes |
| `mkdir personal` | Make a new directory in the current working directory (personal folder) |
| `touch new_file.js` | Creating new files in the current working directory |
| `git rm -r [file-name.txt]` | Remove a file (or folder) |

### Branching & Merging

| Command | Description |
| ------- | ----------- |
| `git branch` | List branches (the asterisk denotes the current branch) |
| `git branch -a` | List all branches (local and remote) |
| `git branch [branch name]` | Create a new branch |
| `git branch -d [branch name]` | Delete a branch |
| `git push origin --delete [branch name]` | Delete a remote branch |
| `git checkout -b [branch name]` | Create a new branch and switch to it |
| `git checkout -b [branch name] origin/[branch name]` | Clone a remote branch and switch to it |
| `git branch -m [old branch name] [new branch name]` | Rename a local branch |
| `git checkout [branch name]` | Switch to a branch |
| `git checkout -` | Switch to the branch last checked out |
| `git checkout -- [file-name.txt]` | Discard changes to a file |
| `git merge [branch name]` | Merge a branch into the active branch |
| `git merge [source branch] [target branch]` | Merge a branch into a target branch |
| `git stash` | Stash changes in a dirty working directory |
| `git stash clear` | Remove all stashed entries |

### Sharing & Updating Projects

| Command | Description |
| ------- | ----------- |
| `git push origin [branch name]` | Push a branch to your remote repository |
| `git push -u origin [branch name]` | Push changes to remote repository (and remember the branch) |
| `git push` | Push changes to remote repository (remembered branch) |
| `git push origin --delete [branch name]` | Delete a remote branch |
| `git pull` | Update local repository to the newest commit |
| `git pull origin [branch name]` | Pull changes from remote repository |
| `git remote add origin ssh://git@github.com/[username]/[repository-name].git` | Add a remote repository |
| `git remote set-url origin ssh://git@github.com/[username]/[repository-name].git` | Set a repository's origin branch to SSH |

### Push an existing repo in the Main branch

| Command | Description |
| ------- | ----------- |
| `git remote add origin [ssh://git@github.com/[username]/[repository-name].git]` | Add a remote repository |
| `git branch -M main` | Rename current branch to 'main' |
| `git push -u origin main` | Push changes to remote repository (and remember the branch) |

### Inspection & Comparison

| Command | Description |
| ------- | ----------- |
| `git log` | View changes |
| `git log --summary` | View changes (detailed) |
| `git log --oneline` | View changes (briefly) |
| `git diff [source branch] [target branch]` | Preview changes before merging |

### Delete Past Commits History if any error arises 
#### Remove all the past commits in main branch and keeping the files in a new orphan branch later renaming it to main branch

| Command | Description |
| ------- | ----------- |
| `git checkout --orphan` | Create a New branch of the Current / Main / Master Branch |
| `git add .` | Use this to access root directory (ONLY) |
| `git commit -m "[commit message your message here as example: deleted]"` | Commit changes & name |
| `git branch -D main` | Delete main branch |
| `git branch -m main` | Rename current branch to 'main' |
| `git push -f origin main` | Push & Finish |

### Gitignore specifies the patterns of files and directories that won't be tracked by git
#### Typically to avoid and untrack directory files, outputs, data, binaries, Distribution / packaging-packages, installer/installer logs, dll files, extensions, env files etc. being checked in.

| Command | Description |
| ------- | ----------- |
| `touch .gitignore` | Creating a file mainly gitignore |
| Save this in the gitignore file | Description |
| `personal/ [and in next line] something.js` | For instance exlude personal folder and something.js hence this file won't be tracked in our version control system|

### Git LFS (Large File Storage)

| Command | Description |
| ------- | ----------- |
| `git lfs install` | Download and install the Git command line extension |
| `git lfs track "*.resources"` | Select the file types you'd like Git LFS to manage (or directly edit your .gitattributes) Example: tracking *.resources (tracking all files with resources as extension) |
| `git add .gitattributes` | Now make sure .gitattributes is tracked |
| `git status` | To make sure check status in which branch you are currently in |
| `git add [file-name.txt]` | Add a file to the staging area (Example: git add . ) . all the files in root directory or for instance file.psd / file-name.txt |
| `git commit -m "Add Files"` | Commit changes; Here Add Files is a message of that commit |
| `git push origin main` | Push a branch to your main branch; if your current branch is named main |