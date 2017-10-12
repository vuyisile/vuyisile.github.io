A Read–Eval–Print Loop (REPL), also known as an interactive toplevel or language shell, is a simple, interactive computer programming environment that takes single user inputs (i.e. single expressions), evaluates them, and returns the result to the user; a program written in a REPL environment is executed piecewise. The term is most usually used to refer to programming interfaces similar to the classic Lisp machine interactive environment. Common examples include command line shells and similar environments for programming languages, and is particularly characteristic of scripting languages.[1]

Overview

In a REPL, the user enters one or more expressions (rather than an entire compilation unit) and the REPL evaluates them and displays the results. The name read–eval–print loop comes from the names of the Lisp primitive functions which implement this functionality:

    The read function accepts an expression from the user, and parses it into a data structure in memory. For instance, the user may enter the s-expression (+ 1 2 3), which is parsed into a linked list containing four data elements.
    The eval function takes this internal data structure and evaluates it. In Lisp, evaluating an s-expression beginning with the name of a function means calling that function on the arguments that make up the rest of the expression. So the function + is called on the arguments 1 2 3, yielding the result 6.
    The print function takes the result yielded by eval, and prints it out to the user. If it is a complex expression, it may be pretty-printed to make it easier to understand. In this example, though, the number 6 does not need much formatting to print.

The development environment then returns to the read state, creating a loop, which terminates when the program is closed.

REPLs facilitate exploratory programming and debugging because the programmer can inspect the printed result before deciding what expression to provide for the next read. The read–eval–print loop involves the programmer more frequently than the classic edit-compile-run-debug cycle.

Because the print function outputs in the same textual format that the read function uses for input, most results are printed in a form that could (if it is useful) be copied and pasted back into the REPL. However, it's sometimes necessary to print representations of elements that can't sensibly be read back in, such as a socket handle or a complex class instance. In these cases, there must exist a syntax for unreadable objects. In Python, it is the <__module__.class instance> notation, and in Common Lisp, the #<whatever> form. The REPL of CLIM, SLIME, and the Symbolics Lisp Machine can also read back unreadable objects. They record for each output which object was printed. Later when the code is read back, the object will be retrieved from the printed output.

REPLs can be created to support any language. REPL support for compiled languages is usually achieved by implementing an interpreter on top of a virtual machine which provides an interface to the compiler. Examples of REPLs for compiled languages include CINT (and its successor Cling) and Ch for C/C++, and BeanShell and JShell for Java.
Uses

As a shell, a REPL environment allows users to access relevant features of an operating system in addition to providing access to programming capabilities.

The most common use for REPLs outside of operating system shells is for instantaneous prototyping. Other uses include mathematical calculation, creating documents that integrate scientific analysis (e.g. IPython), interactive software maintenance, benchmarking, and algorithm exploration.

A REPL can become an essential part of learning a new language as it gives quick feedback to the novice.
Implementation

To implement a Lisp REPL, it is necessary only to implement these three functions and an infinite-loop function. (Naturally, the implementation of eval will be complicated, since it must also implement all the primitive functions like car and + and special operators like if.) This done, a basic REPL itself is but a single line of code:

(loop (print (eval (read))))

One possible implementation of eval is as a recursive interpreter that acts on the abstract syntax tree created by read. Another possibility is to compile the syntax tree into machine code and execute it.

Real REPL implementations in Lisp are often much more complicated.
Functionality

Typical functionality provided by a Lisp REPL includes:

    History of inputs and outputs.
    Variables are set for the input expressions and results. These variables are also available in the REPL. For example in Common Lisp * refers to the last result, ** and *** to the results before that.
    Levels of REPLs. In many Lisp systems if an error occurs during the reading, evaluation or printing of an expression, the system is not thrown back to the top-level with an error message. Instead a new REPL, one level deeper, is started in the error context. The user can then inspect the problem, fix it and continue - if possible. If an error occurs in such a debug REPL, another REPL, again a level deeper, is started. Often the REPL offers special debug commands.
    Error handling. The REPL provides restarts. These restarts can be used, when an error occurs, to go back to a certain REPL level.
    Mouse sensitive input and output of data objects.
    Input editing and context specific completion over symbols, pathnames, class names and other objects.
    Help and documentation for commands.
    Variables to control the reader. For example, the variable *read-base* controls in which base numbers are read by default.
    Variables to control the printer. Example: maximum length or maximum depth of expressions to print.
    Additional command syntax. Some REPLs have commands that follow not the s-expression syntax, but often work with Lisp data as arguments.
    Graphical REPLs. Some Lisp REPLs (the CLIM Listener is an example) accept also graphical input and output.

References

    Hey, Tony; Pápay, Gyuri (2014). The Computing Universe: A Journey through a Revolution. Cambridge University Press. p. 76. ISBN 978-1-31612322-5, "A major characteristic of modern scripting languages is their interactivity, sometimes referred to as a REPL programming environment. ... The characteristics of ease of use and immediate execution with a REPL environment are sometimes taken as the definition of a scripting language."

External links

    Paul Graham has written a description of a REPL implementation in Common Lisp.
    Joël Franusic Online-REPs-and-REPLs list
    repl.it is a client-side web REPL for various programming languages.

