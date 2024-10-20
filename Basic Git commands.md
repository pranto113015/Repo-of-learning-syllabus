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


#### Working flow gihub

undo changs ( working directory-> stagging area-> local repo-> remote-repo)

```sh
git checkout -- . (undo from unstaging)
git reset HEAD . (undo from stagging )
git reset -hard HEAD . (undo from stagging & unstaging)
```





#### Set vs code github account by git bash terminal

```sh
git config --global user.name "github user name this area"
```
```sh
git config --global user.email "github user email this area"
```




#### git clone command

```sh
git clone <url>
```

#### Multiple commit title with sub title

```sh
git commit -m "main title" -m "sub title 1" -m "sub title 2"
```


#### vs code shotcut

keyboard shortcut with the backtick character to show or hide the terminal window `Use the Ctrl + ` 



#### Changing git commit message after latest push  

First...
```bash
git commit --amend -m "<write new message>"
```
Then...
```bash
git push --force origin <branch-name>
```














