# Git
- Git is a version-control system.
- Git is free & open-source. :-)

- Check out Ian Schoonover for videos on Git & Github
https://www.youtube.com/watch?v=wTHPBO28nYQ&list=PL86ehqHzxhy4XX_qZZE_5mrp38WGZRzTO&index=18

## Basics
### git init
- Initialises the current dir as a Git repository by making a .git directory, this tracks any changes

### git status
- Shows the current status of the current repo

### git add <<.> || <DIRNAME>>
- Adds files for git to track

### git commit
- Commits the the currently tracked files, add -m "message here" to add a commit message

### What does "nothing to commit, working tree clean" mean?
- There are no changes, untracked or tracked, waiting to be processed

## Git Checkout
### git log
- Shows all commit logs, use arrows to navigate.
- 'q' to exit

### git checkout <COMMIT-CODE-FROM-GIT-LOGS>
- Will not lot you checkout without commiting any uncommited files
- Changes your current branch(master) to the branch of the version specified
- Usually used to check out some old code haha

#### What is 'master'?
- Master is the main branch for your code
                  | HEAD
v1 -> v2 -> v3 -> v4
                  | Master

#### What is 'HEAD'?
- HEAD is a pointer for what branch you are currently looking at
- The HEAD can be detatched from the 'master'
| HEAD
v1 -> v2 -> v3 -> v4
                  | Master

#### How to point the HEAD back at the master branch?
- Use 'git checkout master'

#### How to revert a Git repo to a previous version?
- First, use 'git revert --no-commit <COMMIT-HASH-HERE>..HEAD'
This will revert everything from the HEAD back to the commit hash.
It essentially recreates the current commit state to that of the version specified, including all of the working tree.

'--no-commit' reverts all the commits at once, this prevents having to write a message for every commit

- Lastly, use 'git commit' to commit the current state

#### Is it possible to return to a state you originally rolled back from?
- Yes, the commit hash can still be found in 'git logs'

## Github
### First create a git repo on the cli
- git init
### Add & Commit any files
- git add .
- git commit -m "first commit"
### Add the remote github origin to the current git repo
- git remote add origin url
* Push the current commit state to the origin master branch
- git push -u origin master