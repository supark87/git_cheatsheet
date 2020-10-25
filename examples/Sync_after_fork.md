
# After Fork 

`git remote add upstream <url>`

: This command is for synchronize your forked repository on your local computer with changes in original repository you forked from different person's account

For example.

CDC LpSup and local repository.

### Before command

```
(base) ➜  .git git:(main) git remote
origin 
```

### After command

```
(base) ➜  LpSubP-1 git:(master) git remote add upstream git@github.com:CDCgov/LpSubP.git
(base) ➜  LpSubP-1 git:(master) git remote
origin
upstream

(base) ➜  LpSubP-1 git:(master) git remote -v
origin	git@github.com:supark87/LpSubP-1.git (fetch)
origin	git@github.com:supark87/LpSubP-1.git (push)
upstream	git@github.com:CDCgov/LpSubP.git (fetch)
upstream	git@github.com:CDCgov/LpSubP.git (push)
```