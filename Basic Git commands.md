# Basic Git commands

#### Demo repository code by default project


…or create a new repository on the command line
```sh
echo "# Demo-Repository-Pro-2k24" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/pranto113015/Demo-Repository-Pro-2k24.git
git push -u origin main
```

…or push an existing repository from the command line
```sh
git remote add origin https://github.com/pranto113015/Demo-Repository-Pro-2k24.git
git branch -M main
git push -u origin main
```





#### External Command

```sh
git branch
```

```sh
git checkout main
```

```sh
git pull origin main
```

```sh
git branch "newbranchname"
```

```sh
git status
```

```sh
git restore <filename>
```


How To Exit The Git Log? By pressing the q key on the keyboard,we can exit the git log without duplicating the commit default history.

```sh
git log
```

```sh
git log --oneline
```

```sh
git remote
```

```sh
git remote -v
```

```sh
git merge "merge file name"
```

```sh
git commit --amend (correction the commit message)
```

```sh
git revert HEAD (undo a latest commit)
```

```sh
git revert <commit>
```























