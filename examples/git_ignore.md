`git ignore`

- tells Git which files and folders to ignore
- chagnges in ignored files and folders are ignored
- rules are defined in .gitignore
- .gitignore file itself must be commited

- If you want to ignore previously commited file,

` git rm --cached <filename> `

- It will remove the file from repository but keep in working directory



# Generally these are ignored
- bin/

- node_modules/

- compiled and log files like *pyc, *log

-hidden OS files like Thumgs.db or .DS_Store

- "gitignore.io" => choose python and you can copy from it (You can check .gitignore from this site on my repository 'Data_viz_tracking'

- You can also check "github.com/github/gitignore"