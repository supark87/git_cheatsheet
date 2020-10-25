# git show-ref

- This command is used to see local and remote repositories.

- Compare references for different branches

For example, 
```

(base) ➜  Data_viz_tracking git:(main) ✗ git show-ref 
edb0ea78047f00bc89631047c8df3b070f303314 refs/heads/feature-1
000765304022fa94ce630767b8566441804e43a5 refs/heads/jupyternotebook
668efb80c2141c671313584b09b10476439f571f refs/heads/main
668efb80c2141c671313584b09b10476439f571f refs/remotes/origin/HEAD
edb0ea78047f00bc89631047c8df3b070f303314 refs/remotes/origin/feature-1
000765304022fa94ce630767b8566441804e43a5 refs/remotes/origin/jupyternotebook
668efb80c2141c671313584b09b10476439f571f refs/remotes/origin/main


(base) ➜  Data_viz_tracking git:(main) ✗ git show-ref jupyternotebook 
000765304022fa94ce630767b8566441804e43a5 refs/heads/jupyternotebook
000765304022fa94ce630767b8566441804e43a5 refs/remotes/origin/jupyternotebook


```