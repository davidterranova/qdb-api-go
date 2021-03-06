Quasardb Go API
=================
[![GoDoc](https://godoc.org/github.com/golang/gddo?status.svg)](http://godoc.org/github.com/bureau14/qdb-api-go)

**Note:** The Go API works only on Unix-like operating systems. Windows is not currently supported.

**Warning:** Early stage development version. Use at your own risk.

Go API for [quasardb](https://www.quasardb.net/).


### Requirements

1. [Go compiler and tools](https://golang.org/)
1. [quasardb daemon](https://www.quasardb.net/download/index.html)
1. [quasardb C API](https://www.quasardb.net/download/index.html) version corresponding to the OS you use

### Build instructions:
1. go get github.com/bureau14/qdb-api-go
2. Extract the downloaded C API into $GOPATH/src/github.com/bureau14/qdb-api-go/thirdparty/quasardb

### Test instructions:
1.  export QDB_SERVER_PATH=/path/to/qdbd # a path to a working qdbd executable
1b.  export QDB_SERVER_SECURITY_PATH=/path/to/qdb_cluster_keygen # a path to a working qdb_cluster_keygen executable [ if you have a security compatible version of qdbd ]
1c.  export QDB_USER_SECURITY_PATH=/path/to/qdb_user_add # a path to a working qdb_user_add executable [ if you have a security compatible version of qdbd ]
2. cd $GOPATH/src/github.com/bureau14/qdb-api-go
3. go test

### Coverage instructions:
1. export QDB_SERVER_PATH=/path/to/qdbd # a path to a working qdbd executable
2. cd $GOPATH/src/github.com/bureau14/qdb-api-go
3. go test -coverprofile=coverage.out
4. go tool cover -html=coverage.out # if you want to see coverage detail in a browser

### Usage (OS X)
1. mkdir $GOPATH/src/<PROJECT>
2. Extract the downloaded C API into $GOPATH/src/<PROJECT>/thirdparty/quasardb
3. Ensure Quasar C lib is in the **DYLD_LIBRARY_PATH** : `export DYLD_LIBRARY_PATH=$DYLD_LIBRARY_PATH:$GOPATH/src/<PROJECT>/thirdparty/quasardb/lib`

### Troubleshooting

If you encounter any problems, please create an issue in the bug tracker.
