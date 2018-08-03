#### SSH key
##### Generate SSH key
```ssh-keygen -t rsa -C "your.email@example.com" -b 4096```
##### Add SSH key
```
eval $(ssh-agent -s)
ssh-add ~/.ssh/id_rsa
```
##### Copy the ssh key into your Github/Lab account
```cat ~/.ssh/id_rsa.pub```
#### Global config 
##### Don't forget to put your real name and email 
```
git config --global user.name "Mona Lisa"
git config --global user.email "your.email@example.com"
```
#### Alias
- git config --global alias.co checkout 
- git config --global alias.br branch 
- git config --global alias.ci commit 
- git config --global alias.st status 
- git config --global alias.ps push 
#### Branch
##### Delete local branch
```git branch -d the_local_branch```
##### List local branch
```git branch```
##### List remote branch
```git branch -r```
##### Modify name to master
```
git branch -m master
git push origin master
```
#### Release
- git checkout release/X
- git merge --no-ff feature/A
- git merge --no-ff feature/B
- git push origin release/X
#### Stash
##### List 
```git stash list```
##### Save stash with a name
```git stash save "My Message"```
##### Apply and Drop first stash
```git stash pop```
##### Apply stash n
```git stash apply stash@{n}```
##### See detail stash n
```git stash show stash@{n} -p```
#### Gitignore
##### if files are not ignore
```
git rm --cached -r .
git add .
```
#### Commit
##### Change commit message
```git commit --amend```
##### Undo the last commit (leave the changes available)
```git reset HEAD~ --soft```
##### Undo the last commit (remove changes)
```git reset HEAD~ --hard```
#### Rebase master in feature/X
- git checkout feature/X
- git fetch --all
- git rebase origine/master
- fix conflits in PHPStorm (Local Changes -> Right Click -> Git -> Resolve Conflit)
- git rebase --continue
- git push -f origin feature/X
