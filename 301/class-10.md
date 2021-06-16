# What is a ‘call’?
A call stack is a mechanism for an interpreter (like the JavaScript interpreter in a web browser) to keep track of its place in a script that calls multiple functions — what function is currently being run and what functions are called from within that function, etc.

# How many ‘calls’ can happen at once?
The maximum call stack size ranges from 10 to 50 thousand calls, so if you exceed that, it's most likely that you have an infinite loop in your code. The browser prevents your code from freezing the whole page by limiting the call stack. I re-created the error with the following code.

# How many ‘calls’ can happen at once?
At the most basic level, a call stack is a data structure that uses the Last In, First Out (LIFO) principle to temporarily store and manage function invocation (call).

# Draw an example of a call stack and the functions that would need to be invoked to generate that call stack.
A stack overflow occurs when there is a recursive function (a function that calls itself) without an exit point. The browser (hosting environment) has a maximum stack call that it can accomodate before throwing a stack error.
***The callMyself() will run until the browser throws a “Maximum call size exceeded”.***


# What is a ‘refrence error’?
The ReferenceError object represents an error when a non-existent variable is referenced.

# What is a ‘syntax error’?
The SyntaxError object represents an error when trying to interpret syntactically invalid code. It is thrown when the JavaScript engine encounters tokens or token order that does not conform to the syntax of the language when parsing code.

# What is a ‘range error’?
It means that somewhere in your code, you are calling a function which in turn calls another function and so forth, until you hit the call stack limit. This is almost always because of a recursive function with a base case that isn't being met.

# What is a ‘tyep error’?
The TypeError object represents an error when an operation could not be performed, typically (but not exclusively) when a value is not of the expected type. A TypeError may be thrown when: an operand or argument passed to a function is incompatible with the type expected by that operator or function.

# What is a breakpoint?
At each breakpoint, JavaScript will stop executing, and let you examine JavaScript values. After examining values, you can resume the execution of code (typically with a play button).

# What does the word ‘debugger’ do in your code?
The debugger statement stops the execution of JavaScript, and calls (if available) the debugging function. Using the debugger statement has the same function as setting a breakpoint in the code. Normally, you activate debugging in your browser with the F12 key, and select "Console" in the debugger menu.