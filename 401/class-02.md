# Testing and Modules:

## Test-Driven Development with Python

TDD isn’t something that comes naturally. It’s a discipline, like a martial art, and just
like in a Kung Fu movie, you need a bad-tempered and unreasonable master to force
you to learn the discipline.
the first step in web development is getting your web framework installed
and configured. Download this, install that, configure the other, run the script…but
TDD requires a different mindset.
In TDD the first step is always the same: write a test.
First we write the test; then we run it and check that it fails as expected. Only then do
we go ahead and build some of our app.
Unit tests are some pieces of code to exercise the input, the output and the behaviour of your code. You can write them anytime you want.
But Test-Driven Development is a strategy to think (and write!) tests first.
There are some details to pay attention. The first one is the test name. The tests can be considered as your alive documentation.

## If name equals main:

the main qustion is: What does the if **name** == “**main**”: do????
'**main**' is the name of the scope in which top-level code executes. A module’s **name** is set equal to '**main**' when read from standard input, a script, or from an interactive prompt.

A module can discover whether or not it is running in the main scope by checking its own **name**, which allows a common idiom for conditionally executing code in a module when it is run as a script or with python -m but not when it is imported:
#################################################
if **name** == "**main**": # execute only if run as a script
main()
##################################################  
For a package, the same effect can be achieved by including a **main**.py module, the contents of which will be executed when the module is run with -m.

# Recursion:

computer program consists of line-by-line instructions. The computer performs those instructions line-by-line. However, some instructions may be repetitive with a common pattern. Recursion or iteration helps one to write a few lines of codes to perform such repetitive tasks. Suppose a Python list with five-string elements. We wish to print the elements one in a line. This operation needs five lines of codes.
It can be observed that the five lines of codes follow the same pattern. The only difference in each line is the index of the list elements. What if this list contains 100 or 1000 elements? Coding will become a tedious task. These kinds of problems are resolved through either iteration or recursion.
Recursion is a functional approach of breaking down a problem into a set of simple subproblems with an identical pattern and solving them by calling one subproblem inside another in sequential order. Recursion is executed by defining a function that can solve one subproblem at a time. Somewhere inside that function, it calls itself but solving another subproblem. Thus, the call to itself continues until some limiting criteria is met.

The first call to a recursive function from the main program will be returned only after all the subcalls are finished. Hence, Python stores the results of all subproblems in temporary memory, executes some arithmetic operations (if needed), and releases the memory after the end of recursion.
Iterations are performed through ‘for’ and ‘while’ loops. Iterations execute a set of instructions repeatedly until some limiting criteria is met. In contrast to recursion, iteration does not require temporary memory to keep on the results of each iteration. Rather, programmers should define a variable (a number, or list, or string, or any mutable data type) well before the start of iterative calls to collect the results (if there are such arithmetic results) during each iteration.
Note that both recursive and iterative programs have the same problem-solving powers, i.e., every recursive program can be written iteratively and vice versa is also true. The recursive program has greater space requirements than iterative program as all functions will remain in the stack until the base case is reached. It also has greater time requirements because of function calls and returns overhead.

**_the last part of reading is talking about list in python and for and in method beside that also about the strings and decumentation and how we can wreite small testable peice of code and the last part is kind of totrials for testing with different examples_**
