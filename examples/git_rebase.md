#destructive 

- history linear (single parent for each commit)
- rewrites history 
- does not keep entire history of all commits

1. Checkout feature branch 
`git checkout feature1`

2. Rebase feature branch on top of the base branch
`git rebase master`

3. checkout base branch
`git checkout master`

4. Merge feature branch into the base branch. Fast forward merge will be used
`git merge feature1`


## Advanced : rebase with squashing -> Makes several commits on one branch as one commit

- You can choose when you merge from pull request

```
commit e67953179b65264926e9ccdaae2d7a26461e1c2a (HEAD -> main, origin/main, origin/HEAD)
Author: supark87 <32421592+supark87@users.noreply.github.com>
Date:   Tue Oct 20 23:30:32 2020 -0400

    Feature1 created several files  (#1)
    
    * create new files
    
    * create file4.txt

```

## squashing with interactive (-i)

```
(base) ➜  rebasing_with_squashing git:(feature2) git rebase -i e67953179b
[detached HEAD f3dcd0b] file 5 was created in feature2 branch
 Date: Tue Oct 20 23:35:40 2020 -0400
 3 files changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 file5.txt
 create mode 100644 file6.txt
 create mode 100644 file7.txt
Successfully rebased and updated refs/heads/feature2.
```

change pick to s(squash)


```
commit f3dcd0b991dc26d9c1949579c190a2ccbfde9ddd (HEAD -> feature2)
Author: Subin <supark87@gmail.com>
Date:   Tue Oct 20 23:35:40 2020 -0400

    file 5 was created in feature2 branch
    
    file 6 was created in feature2 branch
    
    file 7 was created in feature2 branch

```

Then    `git merge feature2`

```
(base) ➜  rebasing_with_squashing git:(main) git merge -v feature2
Updating e679531..f3dcd0b
Fast-forward
 file5.txt | 0
 file6.txt | 0
 file7.txt | 0
 3 files changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 file5.txt
 create mode 100644 file6.txt
 create mode 100644 file7.txt
```

