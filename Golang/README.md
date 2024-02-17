# Introduction

Go also known as Golang is an open source, compiled and statically typed programming language developed by Google.
Go is a general-purpose programming language with a simple syntax and is backed by a robust standard library. One of the key areas where Go shines is the creation of highly available and scalable web apps. Go can also be used to create command-line applications, desktop apps and even mobile applications.

## Advantages of Go

### 1- Simple syntax
The syntax is simple and concise and the language is not bloated with unnecessary features. This makes it easy to write code that is readable and maintainable.

### 2- Easy to write concurrent programs
Concurrency is an inherent part of the language. As a result, writing multithreaded programs is a piece of cake. This is achieved by Goroutines and channels which we will discuss in the upcoming tutorials.

### 3- Compiled language
Go is a compiled language. The source code is compiled to a native binary.

### 4- Fast compilation
The Go compiler is pretty amazing and it has been designed to be fast right from the beginning.

### 5- Static linking
The Go compiler supports static linking. The entire Go project can be statically linked into one big fat binary and it can be deployed in cloud servers easily without worrying about dependencies.

### 6- Go Tooling
Tooling deserves a special mention in Go. Go comes bundled with powerful tools that help developers write better code. Few of the commonly used tools are,

- gofmt - gofmt is used to automatically format go source code. It uses tabs for indentation and blanks for alignment.
- vet - vet analyses the go source code and reports possible suspicious code. Everything reported by vet is not a genuine problem but it has the capability to catch errors that are not reported by the compiler such as incorrect format specifiers when using Printf.
- staticcheck - staticcheck is used to enforce styling issues in the code.

### 7- Garbage collection

Go uses garbage collection and hence memory management is pretty much taken care automatically and the developer doesn’t need to worry about managing memory. This also helps to write concurrent programs easily.

## Creating a Go Module

Go modules are used to track our application’s dependencies and their versions.
Run `go mod init learngo` inside the `~/Documents/learngo/` directory. This will create a file named go.mod. The contents of the file are provided below.
```
module learngo

go 1.17
```