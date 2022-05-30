### TTD: Test-Driven Development

It is a strategy in software development where tests are developed to validate and test the code and what it will do
before it is fully developed, and it is opposed to software being developed and then tested.
It is used to improve debugging.

### if __name__ == “__main__”

Python files are called modules and they are identified by the .py file extension.
A module can define functions, classes, and variables.
So when the interpreter runs a module, the __name__ variable will be set as  __main__ if the module
that is being run is the main program.
But if the code is importing the module from another module, then the __name__  variable will be set to that module’s name.

### Recursion


It is a way in programming, where the function is called inside its body. It is used to solve complex problems and save time and effort. A famous example of recursion is computing the factorial of a number. 

factorial(n) = n * factorial(n-1)
.
.
.
factorial(1) = 1

It is important when using recursion to make sure that we have an ending point for the recursion so that it would not recurse infintly 