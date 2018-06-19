# Git

All branches
```
git branch -v -a
```

Rename branch
```
git branch -m <oldname> <newname>
git branch -m <newname>
```

Remote info
```
git remote -v
```

Add remote
```
git remote add origin git@github.com:<username>/<repo>
```

Remove remote
```
git remote rm git@github.com:<username>/<repo>
```

Push new branch to origin
```
git push --set-upstream origin <branch-name>
```

User info, remove `--global` to update data only in the current repo
```
git config --global user.name
git config --global user.name "<name>"
git config --global user.email
git config --global user.email "<email>"
```
