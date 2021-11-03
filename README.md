# git
this repo is used to document helpful git commands and procedures

## revert a single file to last commit
step 1. find the commit ID
`git log ./t-vector.cpp`
step 2. copy the right commit ID, for example
 `5f249e5c0a71634dfbc835b3c47da2d198279c50` 
 from 
```
commit 5f249e5c0a71634dfbc835b3c47da2d198279c50
Author: Danjie Hu <danjiehu@outlook.com>
Date:   Mon Nov 1 22:23:28 2021 +0800

    vector of user defined types demo completed
```
step 3. check out, with ** --./file-path.cpp ** and recommit
```
git checkout 5f249e5c0a71634dfbc835b3c47da2d198279c50 -- t-vector.cpp

git add .
git commit -m "reverted back from a failed compile to completed cout single vector[i] demo"
```
