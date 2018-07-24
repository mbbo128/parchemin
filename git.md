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
