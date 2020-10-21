# git log with oneline, graph, stat


`git log --oneline`

You can see commits oneline -> more condensed

For example,

```
commit cdde5256521366346e2a4b0ad82be3d21938f63d (HEAD -> master, origin/master, origin/HEAD)
Author: Eldo <eldin.talundzic@icloud.com>
Date:   Wed Oct 14 15:32:07 2020 -0400

    README pointing to stable release

commit 6d165f3867c2a0d37eead55235cc683891452fed
Author: Eldin Talundzic <31478239+eldin-talundzic@users.noreply.github.com>
Date:   Tue Oct 13 16:34:16 2020 -0400

    House keeping/cleaning

commit 0d565bf682cf8533d9d190cab6d3ee20c448d8f7
Author: Eldin Talundzic <31478239+eldin-talundzic@users.noreply.github.com>
Date:   Tue Oct 13 16:34:02 2020 -0400

    House keeping/cleaning
```

vs

```
cdde525 (HEAD -> master, origin/master, origin/HEAD) README pointing to stable release
6d165f3 House keeping/cleaning
0d565bf House keeping/cleaning
e1c0e8e Merge pull request #3 from supark872/patch-1
8b35acf Update README.md
98e1dbe Merge branch 'yyr4-patch-1-1'
dbd7d5c add OSX install info
6ed9d59 Update README.md
cd8a184 Merge pull request #2 from ohjeyy93/Nest-comments
7a9b67d Add files via upload
fd1f9bd This is a new commit for what I originally planned to be amended
c88c2c3 cleaning

```


`git log --graph` or `git log --graph --oneline`

Shows all parents


```* commit cdde5256521366346e2a4b0ad82be3d21938f63d (HEAD -> master, origin/master, origin/HEAD)
| Author: Eldo <eldin.talundzic@icloud.com>
| Date:   Wed Oct 14 15:32:07 2020 -0400
| 
|     README pointing to stable release
| 
* commit 6d165f3867c2a0d37eead55235cc683891452fed
| Author: Eldin Talundzic <31478239+eldin-talundzic@users.noreply.github.com>
| Date:   Tue Oct 13 16:34:16 2020 -0400
| 
|     House keeping/cleaning
| 
* commit 0d565bf682cf8533d9d190cab6d3ee20c448d8f7
| Author: Eldin Talundzic <31478239+eldin-talundzic@users.noreply.github.com>
| Date:   Tue Oct 13 16:34:02 2020 -0400
| 
|     House keeping/cleaning
|   
*   commit e1c0e8e5e739760e3606413f61a11d5a29eeb2da
|\  Merge: 98e1dbe 8b35acf
| | Author: Eldin Talundzic <31478239+eldin-talundzic@users.noreply.github.com>
| | Date:   Tue Oct 13 16:30:23 2020 -0400
| | 
| |     Merge pull request #3 from supark872/patch-1
| |     
| |     Update README.md
| | 
| * commit 8b35acfcce895536d2af3971b5aa3788e4eec840
|/  Author: supark872 <72620146+supark872@users.noreply.github.com>
|   Date:   Tue Oct 13 15:46:29 2020 -0400
|   
|       Update README.md
|   
*   commit 98e1dbe72ea4c5a306c1b6effdbf969dbb680e56
|\  Merge: 6ed9d59 dbd7d5c
| | Author: Eldo <eldin.talundzic@icloud.com>
| | Date:   Tue Oct 13 14:59:51 2020 -0400
| | 
| |     Merge branch 'yyr4-patch-1-1'
| |     
| |     Adding bed file fix and directions on installing on OSX system
| |     (Catalina)
| | 
| * commit dbd7d5c2480486e04253e293b140af6b44edebb0
| | Author: Eldo <eldin.talundzic@icloud.com>
| | Date:   Tue Oct 13 14:57:05 2020 -0400
| | 
| |     add OSX install info
:
```

git log --stat
```
commit cdde5256521366346e2a4b0ad82be3d21938f63d (HEAD -> master, origin/master, origin/HEAD)
Author: Eldo <eldin.talundzic@icloud.com>
Date:   Wed Oct 14 15:32:07 2020 -0400

    README pointing to stable release

 README.md | 320 +------------------------------------------------------------------------------------------------------------
 1 file changed, 1 insertion(+), 319 deletions(-)

commit 6d165f3867c2a0d37eead55235cc683891452fed
Author: Eldin Talundzic <31478239+eldin-talundzic@users.noreply.github.com>
Date:   Tue Oct 13 16:34:16 2020 -0400

    House keeping/cleaning

commit 0d565bf682cf8533d9d190cab6d3ee20c448d8f7
Author: Eldin Talundzic <31478239+eldin-talundzic@users.noreply.github.com>
Date:   Tue Oct 13 16:34:02 2020 -0400

    House keeping/cleaning

 README.md | 8 +++-----
 1 file changed, 3 insertions(+), 5 deletions(-)

commit e1c0e8e5e739760e3606413f61a11d5a29eeb2da
Merge: 98e1dbe 8b35acf
Author: Eldin Talundzic <31478239+eldin-talundzic@users.noreply.github.com>
Date:   Tue Oct 13 16:30:23 2020 -0400

    Merge pull request #3 from supark872/patch-1
    
    Update README.md

```

` git shortlog ` (-e -n -s)
 You can see by authors

 ```
 Eldin Talundzic (5):
      updating install.sh for OSX
      Update README.md
      Merge pull request #3 from supark872/patch-1
      House keeping/cleaning
      House keeping/cleaning

Eldo (7):
      added date to Readme
      update OSX preq
      fix install OSX & prereq added
      cleaning
      add OSX install info
      Merge branch 'yyr4-patch-1-1'
      README pointing to stable release

Shashidhar Ravishankar (354):
      Annotate calls changed; BBMap and Kestrel need to be added; Visualization framework needs to added
      Runs BWA MEM; BBMap and Bowtie needs to added
      Full fledged VCF parser added
      Removed bed flag in bcftools command
      Annotate variants given a bed file
      Example results files
```

`git log --author="Eldo" ' (--oneline)

Filter logs by author

`git log --grep = "v2.0.0" ' (--oneline)

```
commit 8aed92531e0f706e75b8d67ad54700fb9667132a
Merge: 4347437 4cf7043
Author: Shashidhar Ravishankar <shashidhar.r.shankar@gmail.com>
Date:   Sun May 19 17:24:37 2019 -0400

    Merge pull request #9 from shashidhar22/v2.0.1
    
    Updated NeST environment

commit ce6adac844640846f9c77171de5d6435e5c26252
Merge: a7b2558 6c52863
Author: Shashidhar Ravishankar <shashidhar.r.shankar@gmail.com>
Date:   Wed Oct 10 17:47:28 2018 -0400

    Merge pull request #3 from shashidhar22/v2.0.0
    
    V2.0.0

commit e9fe0bc45397f86f43bb0f3a9bf613a6035ec255
Merge: 51abc15 3aa326d
Author: Shashidhar Ravishankar <shashidhar.r.shankar@gmail.com>
Date:   Tue Oct 9 23:13:48 2018 -0400

    Merge branch 'v2.0.0' of github.com:shashidhar22/NeST into v2.0.0

commit be62b04ef9da0546e2671fb600b7792009536615
Merge: 1644fb3 b66e41f
Author: Shashidhar Ravishankar <shashidhar.r.shankar@gmail.com>
Date:   Fri Oct 5 20:17:19 2018 -0400

    Merge branch 'v2.0.0' of github.com:shashidhar22/NeST into v2.0.0
```

` git log --pretty=format="%cn %h"` (name and SHA1 hash) 

` git log --pretty=format:"Author : %cn ; SHA1 hash :%h; Date %cd" ` 

` git log --merges --oneline` : shows merges (useful when there were a lot of merges)

` git log --no-merges --oneline` : shows no merges 



# Git reflog 

- This shows the changes of HEAD also.

For example, 

`git reflog` (And you can checkout to any SHA1)

```
28d1d5 (HEAD -> main) HEAD@{0}: cherry-pick: modify readme.md
fe83f32 (origin/main, origin/HEAD, Enter/main) HEAD@{1}: checkout: moving from temp to main
1053927 (temp) HEAD@{2}: checkout: moving from main to temp
fe83f32 (origin/main, origin/HEAD, Enter/main) HEAD@{3}: checkout: moving from temp to main
1053927 (temp) HEAD@{4}: commit: modify readme.md
e2a0b0a HEAD@{5}: commit: modify file
e8ea4f6 HEAD@{6}: commit: modify revert_exercise.txt
04a1e0b (experimental) HEAD@{7}: checkout: moving from experimental to temp
04a1e0b (experimental) HEAD@{8}: commit: modify file
d2dcae4 HEAD@{9}: commit: modify exercise file
07fe9b3 HEAD@{10}: commit: add git_revert_excercise.txt
0007653 (origin/jupyternotebook, Enter/jupyternotebook, jupyternotebook) HEAD@{11}: checkout: moving from 000765304022fa94ce630767b8566441804e43a5 to experimental
0007653 (origin/jupyternotebook, Enter/jupyternotebook, jupyternotebook) HEAD@{12}: checkout: moving from main to 0007653040
fe83f32 (origin/main, origin/HEAD, Enter/main) HEAD@{13}: commit: add gitignore
```


`git reflog show <branch name> `

- only local but it would be useful when you want to see previous status before any destructive changes in repository 