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

<ins>Declare and Use</ins>: When you initialize or declare a variable in Go, you have to use it. There are no hanging or floating variables
