#Hello world

It's a traditional piece of code that every developer write for the first time.here we have this code but it's important to get familiar with some useful command to how to run, build and etc.
## Environment variables
The `GOPATH` environment variable lists places to look for Go code. On Unix, the value is a colon-separated string. On Windows, the value is a semicolon-separated string. On Plan 9, the value is a list.

`GOPATH` must be set to get, build and install packages outside the standard Go tree.

The Go binary distributions assume they will be installed in /usr/local/go (or c:\Go under Windows), but it is possible to install the Go tools to a different location. In this case you must set the `GOROOT` environment variable to point to the directory in which it was installed.

For example, if you installed Go to your home directory you should add the following commands to `$HOME/.profile`:
```
export GOROOT=$HOME/go
export PATH=$PATH:$GOROOT/bin
```

[What should be the values of GOPATH and GOROOT? stackoverflow](https://stackoverflow.com/questions/7970390/what-should-be-the-values-of-gopath-and-goroot#answer-10847122)
## Basic commands

```
go run <filename>
```
this command helps us to run a go file but if you want to have an executable file you should use one of these
```
go build <filename>
go install <filename>
```
go build just compile the executable file and move it to destination. go install do a little more. it move the executable file to `$GOBIN` or `$GOPATH/bin` and cache all noe-main packages which imported to `$GOPATH/pkg`. the cache will be use in the next compile if it not changed yet.
