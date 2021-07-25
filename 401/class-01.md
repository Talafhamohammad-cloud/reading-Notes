# Behind every seemingly perfect person there's a mess you can't see, this messs is depends on the pain we get from learning so no pain no gain.

## first of all let we start start with O(n):
for the difinition of O(n) we can consider the difinition from the article which is : Big O notation is used in Computer Science to describe the performance or complexity of an algorithm. Big O specifically describes the worst-case scenario, and can be used to describe the execution time required or the space used (e.g. in memory or on disk) by an algorithm.
and we can ctigorized ity mathematicaly as follows :
1-Θ-notation – asymptotic lower and upper bound:
***Θ(g(n))={f(n):there exist positive constant c1,c2 and n0 such that 0<=c1g(n)<=f(n)<=c2g(n) for all n>=n0}***

2-Ο-notation – asymptotic upper bound:
***Θ(g(n))={f(n):there exist positive constant c and n0 such that 0<=f(n)<=cg(n) for all n>=n0}***

3-Ω-notation – asymptotic lower bound:
***Θ(g(n))={f(n):there exist positive constant c and n0 such that 0<=cg(n)<=f(n) for all n>=n0}***
and here is some examples of growth of function:
1-O(1) describes an algorithm that will always execute in the same time (or space) regardless of the size of the input data set.

2-O(N) describes an algorithm whose performance will grow linearly and in direct proportion to the size of the input data set. The example below also demonstrates how Big O favours the worst-case performance scenario; a matching string could be found during any iteration of the for loop and the function would return early, but Big O notation will always assume the upper limit where the algorithm will perform the maximum number of iterations.

3-O(N²) represents an algorithm whose performance is directly proportional to the square of the size of the input data set. This is common with algorithms that involve nested iterations over the data set. Deeper nested iterations will result in O(N³), O(N⁴) etc.

4-O(2^N) denotes an algorithm whose growth doubles with each addition to the input data set. The growth curve of an O(2^N) function is exponential — starting off very shallow, then rising meteorically. An example of an O(2^N) function is the recursive calculation of Fibonacci numbers:

5-Logarithms 
## Additional Resources:

the are explaining the big O notation beside that the linked list so we can defined it briefly as :
A linked list is a data structure in which the objects are arranged in a linear order.Unlike an array, though, in which the linear order is determined by the array indices, the order in a linked list is determined by a pointer in each object.
In the doubly linked lists along the key field there are two pointer fields: prev[x] points to the previous, and next[x] points to the next element of the list.
If head[L]=NIL, then the list is empty, if next[x]=NIL, then x is the first element of the list, and if prev[x]=NIL, then x is the last element of the list.
## Name and values in python:

its talking about python mechanisms:
Python is a very approachable language. Often it works just as you expect if you come to it from other languages.
But you might suddenly encounter surprising behavior.
As in many programming languages, a Python assignment statement associates a symbolic name on the left-hand side with a value on the right-hand side. In Python, we say that names refer to values, or a name is a reference to a value.
all values in Python are mutable. Numbers, strings, and tuples are all immutable. There is no operation on any of these values that can change them in place. All you can do is make new object from old objects.

## Awesome Python Environment:

its talking about How to Setup an Awesome Python Environment for Data Science or any thing else and pyenv command instlation.

## Python Module of the Week (PyMOTW ):
its talking about how to use the modules of the Python 3 standard library.
with some examples 