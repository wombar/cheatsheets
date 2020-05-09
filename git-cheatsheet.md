# Git Cheatsheet

This guide is intended to list out common commands that you may need working as a dev. It's not intended to be a comprehensive guide to git, merely a reference to some basic to advanced commands. 

## Branches

`git branch` - List local branches

`git checkout -b new_branch from_branch` - Create a new branch

`git push origin --delete branch_name` - Delete remote branch

`git branch -d branch_name` - Delete local branch

`git branch -D branch_name` - Delete local branch (with not fully merged message)

`git push -u origin branch_name` - Set upstream on push of local branch

## Staging

### Recover from Errors / Mistakes

`git reset` -  Remove ALL Files from staging area

`git reset -- filename.txt` - Remove a particular file from staging area

`git reset --hard HEAD~1` - Remove the last commit, discarding local changes

`git reset --soft HEAD~1` - Remove the last commit, BUT keep local changes

`git reset 'HEAD@{1}'` - Undo reset commands above

## Rebasing
If you don't understand the risks with rebasing (i.e. everyone hating you) don't use it. Should not be used on remote branches unless you know what you want to do (and so do others). 

### Interactive Rebase
`git rebase -i <commit_hash>`

### Rebase onto remote branch
- Checkout your local branch
- Fetch the latest remote branch
  - `git fetch --all` OR `git fetch origin`
- `git rebase origin/master`

## Forks

### Create a branch from Upstream Branch (e.g. `upstream/master`)
`git checkout -b branch_name upstream/master`

### Change the Remote Tracking Branch
Useful when working with forks and you have created your original branch from `upstream/master`

- `git fetch --all` - Do this first to get the latest set of branches for all your remotes
- `git branch -u origin/remote_branch`

### List remotes
`git remote -v`

### List Branches and their remotes
`git branch -vv`

### Log

`git log --oneline` - One line commits

`git log -5` - Last 5 commits

`git log --stat` - Show how many lines were changed

## Misc
`git fetch --all` - Fetches all branches for all remotes

`git submodule update --init --recursive` - Init and Update submodules 

