
### Getting started

#### Requirements
-------------

- Go version 1.4
- GOPATH
```
$ go help gopath
$ # ensure the PATH contains $GOPATH/bin
$ export PATH=$PATH:$GOPATH/bin
```

#### Get the source code
```
$ go get -u github.com/Zumata/grpc-challenge
```

#### Generate client code
1 First [install protoc](https://github.com/google/protobuf/blob/master/INSTALL.txt)
  - For now, this needs to be installed from source
  - This is will change once proto3 is officially released

2 Install the protoc Go plugin.

```
$ go get -a github.com/golang/protobuf/protoc-gen-go
$
$ # cd into treasurehunt folder and generate client code from game.proto
$  protoc --go_out=plugins=grpc:. game.proto
```
