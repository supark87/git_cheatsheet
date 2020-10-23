# This is good when you don't want to merge branch but just use the same commit to anoter branch


- git checkout -b "temp"
- Make change in README.md (Let's say you will create or modify other files but we only want to reflect changes in README.md)
- git checkout master/main
- git cherry-pick SHA1

# You can also do without commit

- git cherry-pick --no-commit SHA1

- git status -v (see the change)