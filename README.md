# gitplay



-- GIT work area
working directory --- staging --- local repository --- remote repository (online like https://github.com/rahulhegde/gitplay/)

right movement
 - working directory - any local changes 
 - working -> staging - git add
 - staging -> local repoitory - git commit 
 - local repo -> remote repo - git push

left movement 
 - staging -> working	- git restore <filename>
 - local repo -> staging - git restore <filename> --staged
 - remote repo -> local repo - git reset origin/master
 
 also sync the working directory
 - remote repo -> local repo & working directory - git reset --hard origin/master

-- get change from remote repo
git fetch - remote repo to local repo
git pull - remote repo to local repo and working directory 

-- move from 1 branch to another for work

git checkout branch-playcricket-feature
git add -a => git commit -m "cricket feature added"

git checkout branch-playhockey-feature
git branch ==> list which branch is active 
git add => git commit -m "hockey feature added"

-- merge change from branch-source to branch-dest  
git checkout branch-dest  
git merge branch-source // this is equivalent of git commit only you need to push the changes


-- git stash - allows to stash changes on that branch in temporary git space (this is not staging space)
git stash save 
git stash list // list all the stashed changes
git stash apply --index <index_id> // apply the stash changes

OR alternate to stash could be creating a new branch with that temporary changes and commiting
.. do some changes on that branch
git branch <master_featuresave>
git add -a 
git commit -m "temporary stashes branched"
