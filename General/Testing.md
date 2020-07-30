# Testing

## THIS IS SUPER IMPORTANT

### Key Pointers

**High value code**: Any code of good quality has tests, and usually lots of them

**Usually takes around as much time as code**: Proper testing and unit testing should probably take you just as much time to write as do the actual functions that are being tested.

## Types of Tests

### From the Perspective of Features/Access

**Whitebox Testing**: Usually done by developers of a feature; testing that has access and ability to change the code itself.

Generally better when there are very tricky features of the code to test, such as experimenting how a program writes to Stdout, or to a disk, or to a website, etc.

**Blackbox Testing**: Usually done by QA's and testing developers; tests that only know the inputs and outputs of an API, so are really trying to only understand how it works big picture

Often incorporated with exploratory testing; seeing how a package works, importing a github package. 

**Graybox Testing**: Mix of the previous two, where your tests do not have access to the internals of the functions, but are still being built with the intent to test those internals in mind

An example would be of testing in Go, where you have a test package testing a function package, so the test package cannot access the function package's internal variables and commands, but the developer formulates the test package to ensure full code coverage of the tests 