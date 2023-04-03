+++
author = "Sumit Dhiman"
title = "Writing your first Go Lang program"
date = "2023-02-14"
description = "Article to implementing beginners first GO Lang program"
tags = [
    "GO Lang",
    "Code",
    "Hello World",
    "Beginners"
]
categories = [
    "Coding",
    "syntax",
]
series = ["Go Lang"]
aliases = ["Writing Go Lang Code"]
+++

Go is an open-source, statically typed programming language designed to build scalable, secure, easy-to-use systems.
Given that Go Lang was created by **Google**, Google Go is another moniker for it.
It was developed to fill the gap between Java and C++ to provide code that is easy to understand, maintain, and execute without degrading.
Go is a compiled language with features that are comparable to those of C and C++ and share the same initial main function. 

### Installing Go:
- For windows users:  https://go.dev/dl/
- For Linux users:
  - Arch Linux: ``sudo pacman -S go``
  - Debian: ``sudo apt install go``


### Let's start creating our first Hello world code:
- #### First of all create a folder using following command: 
```shell
 mkdir <Your folder>
```
- #### Now `cd` into your folder and create a file named **`main.go`**.
```shell
 cd <Your folder>
 touch main.go
```
- #### Now we need to initialize our go module in this folder.
```shell
go mod init <your module name>
```
- #### We have initiated our module. So, we can start editing our **`main.go`** file.
- #### Here, you can see written `package main`, this determine its package name so that we can import go function from one directory to another.
- #### ``fmt`` package stands for ``format``. It is used to print our data by using ``Println`` function
```go
package main
import "fmt"

func main(){
    fmt.Println("Hello!, World")
}
```
- run and build the program using command below:
```bash
$ go run .
$ go build
```



