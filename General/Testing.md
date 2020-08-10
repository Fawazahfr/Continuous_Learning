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

### Big Picture

**Testing Hierarchy**: <img src="./Graphics/testing_pyramid.png" alt="Test_Pyramid" width="400"/>

**Unit Testing**: Speedy testing that is mapped to a block of code that is meant to go through all the different control flows within that code block. You want to ensure that all the business logic of your code is being run through. The only exceptions to this could be error handling or testing of std library functions being used in your code. 

**Integration Testing**: Test functionality of your block of code/service and other logic/services that it is supposed to work with. This is also written within the code's own code base.

**End to End Testing**: A full scale test suite that goes through a fully automated end to end flow, such as a customer checkout flow from website landing to product order. Lives in its own repo and does it's own thing. Assumes unit tests and integration tests work. Have to code in and check for every part of the process. 

### Special Categories

**Regression Tests**: Tests that intend to catch bugs that may occur upon updates/code changes; bugs that were fixed in a previous section of the code not being directly changed but end up breaking. Important for discovering unintended consequences of new features being added. 

**Acceptance Test**: Most critical tests on code bases; must pass in order for latest version of code to be deployed to production; usually should be well maintained, serve as body guards of the product.

**Functional Test**: Term used lightly in various circumstances, just checks to ensure that things are "functioning"