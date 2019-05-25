
# More commands...
```

git commit --amend -m "Modify readme & add todo.txt"


git reset --soft
git reset --hard <hash-commit>


git reset --hard HEAD^ undo last commit and all changes
git reset --hard HEAD^^ undo last 2 commit and all changes


git config --global alias.st status
git config --global alias.co checkout
git config --global alias.br branch
git config --global alias.ci commit

```

## Edit commit

```
git add .
git commit -m "message"
git commit --amend "edit new message"

```

## Git get some commit

```
git cherry-pick <hash-commit>

```

## Commit some text in file

```
git add -p

y - yes
n - no
q - no and exit
a - yes add this and all
j - pass another

git status


```

## Squash and fixup commit

```

git rebase -i HEAD~2


```



## Branching

```
When you neet other people to work on your branch.
Any branch that will last more than a day

git checkout -b shopping_cart
git push origin shopping_cart

git add card.rb
git commit -a -m "Add new card.rb"

git branch
git branch -r

git checkout shooping_cart
git remote show origin
```

## Tagging

```
A tag is a reference to a commit (used mostly for release versioning)

git tag , list all tag
git checkout <tag-name>, check out code at commit
git tag -a v0.0.3 -m "version 0.0.3"
git push --tags
```

## Rebase Belong to Us

```
Merge commits are bad.
git rebase.
1. Move all changes to master which are not in origin/master to a temporary area.
2. Run all origin/master commits.
3. Run all commits in the temporary area, one at a time.
git rebase --continue
git rebase --abort
git rebase --skip
```

## History and configuration

```
git log
git log --pretty=oneline
git log --pretty=oneline --graph
git log --pretty=oneline --graph --all
filters since
git log --since='Jan 2 2018'
filters until
git log --until='Jan 2 2018'
git log --since='Jan 1 2018' --until='Jan 8 2018'
git log --author='Matheus'
simple log
git shorlog
git shorlog -sn
git reflog
git reflog
git diff
git blame <file-name> --date short
output : commit hash, author, date, line # content

```
