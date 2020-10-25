# git ls-files , git cat-file hash (-p -t -s)


`git ls-files`

: You can see the files in staging-phase

`git cat-file <SHA1hash> -p/-t/-s`

: You can see the type of each SHA1hash. For example, if it is blob, tree, commit, or tag. 
  Also, you can check the parents SHA1 of it. For SHA1, you can just select 4-5 first letters.

  For example, you do `git log` and select SHA1 hash you want to look at.

```

(base) ➜  git_cheatsheet git:(main) git cat-file 7ffce59f1abbf -p
tree 8886020102f089f71ad787506781d78270058caf
parent a90619a317e4eeaf1036c7eeb736eb6d78fdd265
parent 694779d52ac07f7d12bc278ead6f9257e854cedf
author SubinPark <subinpark@adminusers-MBP.attlocal.net> 1603461813 -0400
committer SubinPark <subinpark@adminusers-MBP.attlocal.net> 1603461813 -0400

Merge branch 'main' of github.com:supark87/git_cheatsheet into main
(base) ➜  git_cheatsheet git:(main) git cat-file 7ffce59f1abbf -t
commit
(base) ➜  git_cheatsheet git:(main) git cat-file 7ffce59f1abbf -s
362

```