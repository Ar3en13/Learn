# Introduction

Go also known as Golang is an open source, compiled and statically typed programming language developed by Google.
Go is a general-purpose programming language with a simple syntax and is backed by a robust standard library. One of the key areas where Go shines is the creation of highly available and scalable web apps. Go can also be used to create command-line applications, desktop apps and even mobile applications.

## Advantages of Go

### 1. Simple syntax
The syntax is simple and concise and the language is not bloated with unnecessary features. This makes it easy to write code that is readable and maintainable.

### 2. Easy to write concurrent programs
Concurrency is an inherent part of the language. As a result, writing multithreaded programs is a piece of cake. This is achieved by Goroutines and channels which we will discuss in the upcoming tutorials.

### 3. Compiled language
Go is a compiled language. The source code is compiled to a native binary.

### 4. Fast compilation
The Go compiler is pretty amazing and it has been designed to be fast right from the beginning.

### 5. Static linking
The Go compiler supports static linking. The entire Go project can be statically linked into one big fat binary and it can be deployed in cloud servers easily without worrying about dependencies.

### 6. Go Tooling
Tooling deserves a special mention in Go. Go comes bundled with powerful tools that help developers write better code. Few of the commonly used tools are,

- gofmt - gofmt is used to automatically format go source code. It uses tabs for indentation and blanks for alignment.
- vet - vet analyses the go source code and reports possible suspicious code. Everything reported by vet is not a genuine problem but it has the capability to catch errors that are not reported by the compiler such as incorrect format specifiers when using Printf.
- staticcheck - staticcheck is used to enforce styling issues in the code.

### 7. Garbage collection

Go uses garbage collection and hence memory management is pretty much taken care automatically and the developer doesn’t need to worry about managing memory. This also helps to write concurrent programs easily.

## Creating a Go Module

Go modules are used to track our application’s dependencies and their versions.
Run `go mod init learngo` inside the `~/Documents/learngo/` directory. This will create a file named go.mod. The contents of the file are provided below.
```
module learngo

go 1.17
```

The first line module learngo specifies the module name. The next line go 1.17 indicates that the files in this module use go version 1.17

## Running a go program

There are a couple of different ways to run a Go program. Let’s look at them one by one.

### 1. go install

The first method to run a Go program is using the `go install` command.Let’s cd into the learngo directory we just created.
```
cd ~/Documents/learngo/

```
Run the following command next.

```
go install

```
The above command will compile the program and install(copy) the binary to location `~/go/bin`. The name of the binary will be the name of the go module. In our case, it will be named learngo.

If you want to avoid typing the entire path `~/go/bin/learngo` each time you run the program, you can add `~/go/bin/` to your PATH.

```
export PATH=$PATH:~/go/bin

```
### 2. go build

The second option to run the program is using `go build`. `go build` is much similar to `go install` except that it doesn’t install(copy) the compiled binary to the path `~/go/bin/`, rather it creates the binary inside the location from which `go build` was installed.This command will create a binary named `learngo` in the current directory.Type `./learngo` to run the program.

### 3. go run

One subtle difference between the `go run` and `go build/go install` commands is, `go run` requires the name of the `.go` file as an argument.
Under the hood, `go run` works much similar to `go build`. Instead of compiling and installing the program to the current directory, it compiles the file to a temporary location and runs the file from that location. If you are interested to know the location where go run compiles the file to, please run `go run` with the `--work` argument.

```
go run --work main.go

```




