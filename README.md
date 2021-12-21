# git
this repo is used to document helpful git commands and procedures

## renaming branches
The default branch has been renamed!
main is now named master

If you have a local clone, you can update it by running the following commands.
```
git branch -m main master
git fetch origin
git branch -u origin/master master
git remote set-head origin -a
```

## revert a single file to deserved commit
step 1. see log of commits
```
git log ./t-vector.cpp
```
step 2. find the right commit and copy the commit ID `5f249e5c0a71634dfbc835b3c47da2d198279c50` from 
```
commit 5f249e5c0a71634dfbc835b3c47da2d198279c50
Author: Danjie Hu <danjiehu@email.com>
Date:   Mon Nov 1 22:23:28 2021 +0800

    vector of user defined types demo completed
```
step 3. check out with ** -- ./file-path.cpp ** and recommit
```
git checkout 5f249e5c0a71634dfbc835b3c47da2d198279c50 -- ./t-vector.cpp

git add .
git commit -m "reverted back from a failed compile to completed cout single vector[i] demo"
```
## exit git log
type “q”
