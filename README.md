# gitplay


## GIT work area
working directory --- staging --- local repository --- remote repository (like https://github.com/rahulhegde/gitplay/)

### Right movement of changes
    - working directory - any local changes, saved in editor. 
    - working -> staging - git add
    - staging -> local repoitory - git commit 
    - local repo -> remote repo - git push

### left movement of changes 
    - staging -> working	- git restore <filename>
    - local repo -> staging - git restore <filename> --staged
    - remote repo -> local repo - git reset origin/master
 ### sync the working directory 
    - remote repo -> local repo & working directory - git reset --hard origin/master

### get change from remote repo
    - git fetch - remote repo to local repo
    - git pull - remote repo to local repo and working directory 

### move from 1 branch to another branch for work
    - git checkout branch-playcricket-feature //move branch-playcricket-feature
    - git add -a  // after making changes, updated staging directory
    - git commit -m "cricket feature added" // commit the changes to local repository
    - git checkout branch-playhockey-feature // resume back to original branch-playhockey-feature
    - git branch /// confirm the active branch

### merge change from branch-source to branch-dest  
    - git checkout branch-dest  
    - git merge branch-source   // this is equivalent of git commit only you need to push the changes


### stash changes to temporary git space. This is not staging space
    - git stash save // push or stash the changes temporary 
    - git stash list // list all the stashed changes, this is stored as an indexed list
    - git stash apply --index <index_id> // apply the stash changes

### alternate to stash could be creating a new branch with that temporary changes and commiting
    - git branch <master_featuresave>
    - git add -a 
    - git commit -m "temporary stashes branched"
