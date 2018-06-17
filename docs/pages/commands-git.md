# Git

## All branches
```
git branch -v -a
```

## Rename branch
```
git branch -m <oldname> <newname>
git branch -m <newname>
```

## Remote info
```
git remote -v
```

## Add remote (SSH)
```
git remote add origin git@github.com:<username>/<repo>
```

## Push new branch to origin
```
git push --set-upstream origin <branch-name>
```

## User info
remove `--global` for update dat ain current repo
```
git config --global user.name
git config --global user.name "<name>"
git config --global user.email
git config --global user.email "<email>"
```
