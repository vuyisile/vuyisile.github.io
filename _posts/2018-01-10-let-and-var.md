---
Layout:
Title:  let vs var
Date:   2018-01-10
---

# Variable Scoping

## Overview

In JavaScript we have two types of variables, global and local. A variable that is declared outside a function definition is a global variable,which means the value of that global variable is accessible and modifiable throughout the program. A variable that is decleared in a function is a local variable. It cannot be accessed by any code outside the function, whenever the function is exercuted it gets reset. JavaScript does not support block scope (in which a set of braces {. . .} defines a new scope), except in the special case of block-scoped variables. 

## Javascript Scope

A local variable can have the same name as a global variable, but it is entirely separate; changing the value of one variable has no effect on the other. Only the local version has meaning inside the function in which it is declared. 

        // Global definition of name.  
        var name = "Mark";  

        // A local name variable is declared in this function.  
        function showName(){  
        var name = "Jack";  
        return name +" ,step back please!";
        } 

        console.log(showName());//output: Jack ,step back please!

        name += " ,please go fetch water.";  
        console.log(name);// output: Mark ,please go fetch water.


**Output: "Mark, ,please go fetch water."**  
In JavaScript, variables are evaluated as if they were declared at the beginning of the scope they exist in. Sometimes this results in unexpected behavior, as shown here. 


        var aNumber = 100;  
        tweak();  

        function tweak(){  

            // This prints "undefined", because aNumber is also defined locally below.  
            document.write(aNumber);  

            if (false)  
            {  
                var aNumber = 123;    
            }  
        }  


When JavaScript executes a function, it first looks for all variable declarations, for example, var someVariable;. It creates the variables with an initial value of undefined. If a variable is declared with a value, for example, var someVariable = "something";, then it still initially has the value undefined and takes on the declared value only when the line that contains the declaration is executed. 
JavaScript processes all variable declarations before executing any code, whether the declaration is inside a conditional block or other construct. Once JavaScript has found all the variables, it executes the code in the function. If a variable is implicitly declared inside a function - that is, if it appears on the left side of an assignment expression but has not been declared with var - it is created as a global variable. 
In JavaScript, an inner (nested) function stores references to the local variables that are present in the same scope as the function itself, even after the function returns. This set of references is called a closure. In the following example, the second call to the inner function outputs the same message ("Hello Bill") as the first call, because the input parameter for the outer function, name, is a local variable that is stored in the closure for the inner function. 


        function send(name) {  
            // Local variable 'name' is stored in the closure  
            // for the inner function.  
            return function () {  
                sendHi(name);  
            }  
        }  

        function sendHi(msg) {  
            console.log('Hello ' + msg);  
        }  

        var func = send('Bill');  
        func();  
        // Output:  
        // Hello Bill  
        sendHi('Pete');  
        // Output:  
        // Hello Pete  
        func();  
        // Output:  
        // Hello Bill  


## Block-scoped variables
Internet Explorer 11 introduces support for let and const, which are block-scoped variables. For these variables, the braces {. . .} define a new scope. When you set one of these variables to a particular value, the value applies only to the scope in which it is set. 
The following example illustrates the use of let and block-scoping. 
Note: The following code is supported in Internet Explorer 11 standards mode and later. 

        let x = 10;  
        var y = 10;  
        {  
            let x = 5;  
            var y = 5;  
            {  
                let x = 2;  
                var y = 2;  
                document.write("x: " + x + "<br/>");  
                document.write("y: " + y + "<br/>");  
                // Output:  
                // x: 2  
                // y: 2  
            }  
            document.write("x: " + x + "<br/>");  
            document.write("y: " + y + "<br/>");  
            // Output:  
            // x: 5  
            // y: 2  
        }  

        document.write("x: " + x + "<br/>");  
        document.write("y: " + y + "<br/>");  
        // Output:  
        // x: 10  
        // y: 2  