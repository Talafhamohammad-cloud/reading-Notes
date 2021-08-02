# The Global Scope
Python turns your program’s main script into a module called __main__ 
to hold the main program’s execution. The namespace of this module is the main global scope of your program.
In Python, the notions of global scope and global names are tightly associated with module files. For example, if you define a name at the top level of any Python module, then that name is considered global to the module. That’s the reason why this kind of scope is also called module scope.
To inspect the names within your main global scope, you can use dir(). If you call dir() without arguments, then you’ll get the list of names that live in your current global scope.
You can access or reference the value of any global name from any place in your code. This includes functions and classes.
Whenever you assign a value to a name in Python, one of two things can happen:
-You create a new name
-You update an existing name
The concrete behavior will depend on the Python scope in which you’re assigning the name. If you try to assign a value to a global name inside a function, then you’ll be creating that name in the function’s local scope, shadowing or overriding the global name. This means that you won’t be able to change most variables that have been defined outside the function from within the function.

# nonlocal Statement
Similarly to global names, nonlocal names can be accessed from inner functions, but not assigned or updated. If you want to modify them, then you need to use a nonlocal statement. With a nonlocal statement, you can define a list of names that are going to be treated as nonlocal.

The nonlocal statement consists of the nonlocal keyword followed by one or more names separated by commas. These names will refer to the same names in the enclosing Python scope. The following example shows how you can use nonlocal to modify a variable defined in the enclosing or nonlocal scope:

>>> def func():
...     var = 100  # A nonlocal variable
...     def nested():
...         nonlocal var  # Declare var as nonlocal
...         var += 100
...
...     nested()
...     print(var)
...
>>> func()
200

With the statement nonlocal var, you tell Python that you’ll be modifying var inside nested(). Then, you increment var using an augmented assignment operation. This change is reflected in the nonlocal name var, which now has a value of 200.
Unlike global, you can’t use nonlocal outside of a nested or enclosed function. To be more precise, you can’t use a nonlocal statement in either the global scope or in a local scope.
########################################################################
# video part :
its talking about big o notation with more and more details with several examples and how its work beside its complexcity he also mentiond the space 
and he defined it and expalin it a bit differ in mathematics or we can say he took it from onother aproach.
with several examples  

# Bookmark : 
this part is talking about several examples and how we can generate random numbers then 
he moving on and start talking about data type deep in details .
