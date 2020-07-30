# Golang

## Go Overarching Details

### What Makes Go Different

<ins>Hierarchy</ins>: Go interfaces introduce a feature different from many languages of **no hierarchy**. Interfaces essentially allow certain objects to automatically fall into an interface as long as they match the interface requirements, and don't have to be defined in an 'implements' kind of connection.

<ins>Exceptions</ins>: Go has granular error handling from functions (multiple return statements for functions) that ensure that problems that arise have decisions made for them immediately in terms of how to solve them, rather than massive tri-catch statements. This makes tracking through a stack to find the source of an error much easier, and forces the programmer to consider what an error in each situation means for their application. Is more time consuming however.

<ins>Go Routines</ins>: Concurrent programming with threads is easier in Go with the presence of Go routines. Like a lightweight thread, a function that can run concurrently. Not unusual for Go applications to be running thousands of these at the same time.

### Industry Knowledge

<ins>Microservices</ins>: Go is used frequently in the software world to develop distributed systems with many microservices communicating with one another and running concurrently.

<ins>Kubernetes and Docker</ins>: Docker and Kubernetes are both made with Go, and exemplify how the threading of Go can allow for marvelous backend apps and fluid app deployment in various circumstances, with many complex processes happening at the same time. The distrib. systems community has embraced Go.

## Lang Details

### Rules

<ins>Declare and Use</ins>: When you initialize or declare a variable in Go, you have to use it. There are no hanging variables in Go.

### Cool Features

<ins>Make Command</ins>: Many objects and data types can be instantiated using the make command, like maps, arrays, dictionaries, etc.

<ins>Vendoring</ins>: You can init a mod file in your repo that can list dependencies that can easily be grabbed from github through 'go mod vendor' or individually through 'go get "dependency"' that then adds that item to the go mod file. This means you don't need a package manager in Go to get all of your dependencies. 

### Useful Default Packages

<ins>HTTP</ins>: Go comes with a very useful http package library that allows for many useful functions like routing, http event handling, etc. that makes REST api work much easier.

<ins>Gomock</ins>: You can easily install create mocks for testing using gomock, which is an intelligent automation of mock testable data types for specific tests you've created. 

<ins>Gotests</ins>: Works well with gomock, go tests allows you to create tests (unit, integration, etc. but usually unit) that can be run all at once with an easy test command, allowing a user to ensure regression compatability constantly, and check is small changes don't break everything. It also uses a file name system that allows you to modularize tests and code and various requirements, and helps to ensure that all lines of code are being tested. 

### What Does This Mean

**<-**: This is essentially queueing into the channel to the left of the arrow. If there is nothing to the right, it is like a 'halt and wait for a queue item to come in' line

**Context**: A context is simply a type that carries cancel signals, timed deadlines, and other request-based values and communication between processes and through different APIs. Incoming requests coming to a server should create a context that sets the configurations for that request, and outgoing calls to servers should accept a context to work with. Function calls between two servers must work within the context, and can spawn child contexts from that context. But if the parent context gets cancelled, so do all the children and resources allocated to it. 

**Defer Function**: A defer function is a function whose arguments and setep is evaluated and prepared as soon as it is read, but it does not exectue immediately; rather it is deferred to activating until the function after it executes. Useful for example with cancelling a context after it is utilized in some communication. 

## Testing in Go

### Gotests

Go has built in testing using go tests. Any directory can only have one package within it. The only exception is the package_test package, which tests the initial package.

To create tests that are detected by Go tests, the function name of the test must begin with "Test" like TestThisFunction, and then the bash command "go test" will properly run it.

The use of interfaces is very popular and useful in testing Go functions

1. Rather than feeding the function the arg type that you want specifically, create an interface that matches that arg type, so you can test the function with no side effects that may slow down unit testing, such as needing to actually start a server up. 
   e.g: You have a function that shuts down a server, so you create a shutdownable interface so you can test the shutdown functionality without needing to open an http server 
