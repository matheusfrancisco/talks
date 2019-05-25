## Getting started with git Araramaker.


## Initial Setup
### Git config
```
git config --global user.name "user name here"
git config --global user.email "email here"
git help
git config --global user.name
git config --global user.email
```
## Create a repository

```
git init
```

```
git remote add origin url-repository
git remote -v
```

## Basics commands

```
git status
git add <name-file>
git add .
git add --all
git add *.txt
git add docs/*.txt
git add docs/
git add "*.txt"
git commit -a -m "message"
git commit
git diff
git diff --stage
git log -p
git log -p -1
git log --pretty=online
git log --pretty=short
```

## Edit lasted commit

```
git add file.txt
git commit --amend -m "message"
``` 

## Remove file in stange area

```
git reset <filename>
```

## Discard changes in working directory

```
git checkout -- <file>
```

## Remove files

```
git rm  <filename>
```
