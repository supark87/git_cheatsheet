
`git stash`

- Git creates temperal commit and refs 
- You can go there and work again by 

`git stash pop`



```
(base) ➜  Data_viz_tracking git:(temp) ✗ git stash
Saved working directory and index state WIP on temp: 1053927 modify readme.md
(base) ➜  Data_viz_tracking git:(temp) cat .git/refs/stash
e599d992df9be85e950acfa1ecede02d4494f116
(base) ➜  Data_viz_tracking git:(temp) git cat-file -p e599d992df9be85e950acfa1ecede02d4494f116
tree f03bbffa845f500b680a15920de714ff597acf68
parent 10539274b7dbf1a1e79c912f702a173f9cb3aa13
parent ac3d3784a92517d1144e30b0212d7864387aeae4
author Subin <supark87@gmail.com> 1603248918 -0400
committer Subin <supark87@gmail.com> 1603248918 -0400

WIP on temp: 1053927 modify readme.md%                                                                                         (base) ➜  Data_viz_tracking git:(temp) git cat-file -t e599d992df9be85e950acfa1ecede02d4494f116
commit
(base) ➜  Data_viz_tracking git:(temp) git cat-file -p 105392
tree 0fe09b17d8146de8e6fb3a4b4e0d8bd6bf714588
parent e2a0b0a1fe18ae5ac96dd22e261488a7df9d9c16
author Subin <supark87@gmail.com> 1603248040 -0400
committer Subin <supark87@gmail.com> 1603248040 -0400

modify readme.md
(base) ➜  Data_viz_tracking git:(temp) git cat-file -p ac3d3784a
tree 0fe09b17d8146de8e6fb3a4b4e0d8bd6bf714588
parent 10539274b7dbf1a1e79c912f702a173f9cb3aa13
author Subin <supark87@gmail.com> 1603248918 -0400
committer Subin <supark87@gmail.com> 1603248918 -0400

index on temp: 1053927 modify readme.md
```

```
(base) ➜  Data_viz_tracking git:(temp) git stash pop
On branch temp
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
	modified:   README.md

no changes added to commit (use "git add" and/or "git commit -a")
Dropped refs/stash@{0} (e599d992df9be85e950acfa1ecede02d4494f116)
```