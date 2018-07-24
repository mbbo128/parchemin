#### SSH key
##### Generate SSH key
```ssh-keygen -t rsa -C "your.email@example.com" -b 4096```
##### Add SSh key
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
