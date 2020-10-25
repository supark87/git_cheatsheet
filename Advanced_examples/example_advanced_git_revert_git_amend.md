` git revert HEAD' (Safe, does not modify history, you can revert your mistakes in public repository)

- it will revert the last commit

` git revert SHA1` 

You can check what has been changed by

` git log -p`

For example in Nest,

```
commit cdde5256521366346e2a4b0ad82be3d21938f63d (HEAD -> master, origin/master, origin/HEAD)
Author: Eldo <eldin.talundzic@icloud.com>
Date:   Wed Oct 14 15:32:07 2020 -0400

    README pointing to stable release

diff --git a/README.md b/README.md
index 13cae24..c2474c5 100644
--- a/README.md
+++ b/README.md
@@ -1,319 +1 @@
-# Next-generation Sequence-analysis Toolkit (NeST) : A standardized bioinformatics framework for analyzing SNPs in next-generation sequencing data
-
```


vs 

`git commit --amend -m "New message for the last commit" `

- it will change the last commit, destructive

`git commit --amend -m "New message for the last commit!`

What would be the last commit look like?


`git commit --amend --author= < new info > '

- git amend can only be used for the last commit