# GO
## Install
### Download 
Download the archive and extract it into /usr/local, creating a Go tree in /usr/local/go. 
For example:
```
tar -C /usr/local -xzf go1.14.4.linux-amd64.tar.gz
```
### GOPATH 
Just add the following lines to ~/.bashrc
```
export GOPATH=$HOME/go
export PATH=$PATH:/usr/local/go/bin:$GOPATH/bin
```
## Environment variable 
```
go env
```
## Running 
```
go run
```
or
```
go build inigo.go
./inigo
```
