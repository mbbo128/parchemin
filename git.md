# Git
## SSH key
### Generate SSH key
```ssh-keygen -t rsa -C "your.email@example.com" -b 4096```
### Add SSH key
```
eval $(ssh-agent -s)
ssh-add ~/.ssh/id_rsa
```
### Copy the ssh key into your Github/Lab account
```cat ~/.ssh/id_rsa.pub```
## Global config 
### Don't forget to put your real name and email 
```
git config --global user.name "Mona Lisa"
git config --global user.email "your.email@example.com"
```
## Alias
### Temporary
- git config --global alias.co checkout 
- git config --global alias.br branch 
- git config --global alias.ci commit 
- git config --global alias.st status 
- git config --global alias.ps push 
### Permanent 
```
[alias]
    co = checkout
    br = branch
    ci = commit
    ca = commit --amend
    can = commit --amend --no-edit
    st = status
    ps = push
```
## Branch
### Delete local branch
```git branch -d the_local_branch```
### List local branch
```git branch```
### List remote branch
```git branch -r```
### Modify name to master
```
git branch -m master
git push origin master
```
### Get all branches
git fetch --all
### Get all branches deletes branch who are not in the server
git fetch --prune
## Stash
### List 
```git stash list```
### Stash with untracked
```git stash --include-untracked```
### Save stash with a name
```git stash save "My Message"```
### Apply and Drop first stash
```git stash pop```
### Apply stash n
```git stash apply stash@{n}```
### See detail stash n
```git stash show stash@{n} -p```
## Gitignore
### if files are not ignore
```
git rm --cached -r .
git add .
```
## Commit
### Change commit message
```git commit --amend```
### Change commit message no change commit message
```git commit --amend --no-edit```
### Undo the last commit (leave the changes available)
```git reset HEAD~ --soft```
### Undo the last commit (remove changes)
```git reset HEAD~ --hard```
## Rebase master in feature/X
- git checkout feature/X
- git fetch --all
- git rebase origine/master
- ------------- Only if there are conflits -------------
- fix conflits in PHPStorm (Local Changes -> Right Click -> Git -> Resolve Conflit)
- git rebase --continue
- ------------- Only if there are conflits -------------
- git push -f origin feature/X
## Cherry pick in feature/X from last commit in feature/Y
- git checkout feature/X
- git fetch --all
- git cherry-pick <commit-number-feature/Y>
- ------------- Only if there are conflits -------------
- fix conflits in PHPStorm (Local Changes -> Right Click -> Git -> Resolve Conflit)
- git cherry-pick --continue
- ------------- Only if there are conflits -------------
- git push origin feature/X
## Remove local untracked files 
### Show what will be deleted
```git clean -n```
### Delete directory
```git clean -fd```
### Delete file
```git clean -f```
## Squash Commit
### See log
```git log```
- Commit 1
- Commit 2
- Commit 3
- Master Tag (choose this hash)
### Rebase
```git rebase -i HASH```
- pick commit 1
- s commit 2
- s commit 3
- Save and leave :x
### Finish
git push -f origin feature/X
### Edit squash
```git rebase --edit-todo```
### Cancel squash
git rebase --abort
## Patch
```git diff --cached > /tmp/my.patch```
```git apply /tmp/my.patch```
