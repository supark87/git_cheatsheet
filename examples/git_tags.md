# Static text pointer to specific commit

# Staging(release): Diffrerent feature branches merged into release branch  vs Production (master) :only release branch is merged into master branch

# Sementic versioning 
- v1.1.1 (Major, minor(additional function, minor update), patch(small bug fix))

Light weight (git tag v1.0.0 => stored in the .git/refs/tags)

Annotated (git tag v1.0.0 -m "new tag" => stored in the .git/refs/tags & .git/objects, stores author & date)



#Light weight

` git tag <version> `

```
commit 773852b96368b78c52367dbf5b9c362708304d43 (HEAD -> main, origin/main, origin/HEAD)
Author: Subin <supark87@gmail.com>
Date:   Tue Oct 20 15:08:29 2020 -0400

    modify example1

commit 89a2d6bcae0aea14056dd969c42d0e1516df4870 (tag: v1.0.0)  <= tag stays here(Not like Head pointer)
Author: Subin <supark87@gmail.com>
Date:   Tue Oct 20 14:59:49 2020 -0400

    make examples

commit 8a00f24fff9cbb582f900396b65a4f63cf908605
Author: Subin <supark87@gmail.com>
Date:   Wed Oct 14 22:03:34 2020 -0400

    add folder

commit 52e5774f8f90cb5635eaade912407dd34a21f7bf
Author: Subin <supark87@gmail.com>
Date:   Wed Oct 14 22:01:51 2020 -0400
```

## Push tags to remote
` git push -v --tags `

You can see tags now on this repository 

Now add one more file and push it as v2.1.1 
`git push -v origin v1.0.1`



    add readme


```
(base) ➜  git_cheatsheet git:(main) ✗ cat .git/refs/tags/v1.0.0
89a2d6bcae0aea14056dd969c42d0e1516df4870
```




## Annotated tag

`git tag -a v2.0.0 -m "Initial annoted tag"`

```
(base) ➜  git_cheatsheet git:(main) ✗ git tag -v v2.0.0
object 773852b96368b78c52367dbf5b9c362708304d43
type commit
tag v2.0.0
tagger Subin <supark87@gmail.com> 1603221260 -0400

Initial annoted tag
error: no signature found
(base) ➜  git_cheatsheet git:(main) ✗ cat .git/refs/tags/v2.0.0 
56541d9482c084169a9b90bedf7a92ffc757e09c

```

SHA1 hash is different here since annotated one creates objects

## Push tags to remote repository

`git push -v --tags`

After changes and release patch of it

`git push -v origin v1.0.1'


You can see tags on repository now and do release when you are ready 