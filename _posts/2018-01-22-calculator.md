---
Layout:
Title:  Basic Calculator
Date:   2018-01-22
---

# Basic Javascript Calculator

## Overview

In Free-Code-Camp, I was given a task to create a virtual simple calculator following the user stories provided. Generally a Calculator is defined as something used for making mathematical calculations, 
in particular a small electronic device with a keyboard and a visual display.


## Instructions {user stories}

Objective: Build a CodePen.io app that is functionally similar to this: https://codepen.io/FreeCodeCamp/full/rLJZrA/.

Fulfill the below user stories. Use whichever libraries or APIs you need. Give it your own personal style.

User Story: I can add, subtract, multiply and divide two numbers.

User Story: I can clear the input field with a clear button.

User Story: I can keep chaining mathematical operations together until I hit the equal button, and the calculator will tell me the correct output.

Remember to use Read-Search-Ask if you get stuck.

When you are finished, click the "I've completed this challenge" button and include a link to your CodePen. 

You can get feedback on your project by sharing it with your friends on Facebook.


## My Approach

### Code:

    function pushZero() {
        document.getElementById("input-box").innerHTML += 0;
        return true;
    }
    function pushOne() {
        document.getElementById("input-box").innerHTML += 1;
        return true;
    }
    function pushTwo() {
        document.getElementById("input-box").innerHTML += 2;
        return true;
    }
    function pushThree() {
        document.getElementById("input-box").innerHTML += 3;
        return true;
    }
    function pushFour() {
        document.getElementById("input-box").innerHTML += 4;
        return true;
    }
    function pushFive() {
        document.getElementById("input-box").innerHTML += 5;
        return true;
    }
    function pushSix() {
        document.getElementById("input-box").innerHTML += 6;
        return true;
    }
    function pushSeven() {
        document.getElementById("input-box").innerHTML += 7;
        return true;
    }
    function pushEight() {
        document.getElementById("input-box").innerHTML += 8;
        return true;
    }
    function pushNine() {
        document.getElementById("input-box").innerHTML += 9;
        return true;
    }

    function pushCommaSign() {
        document.getElementById("input-box").innerHTML += '.';
        return true;
    }


    function pushDivideSign() {
        document.getElementById("input-box").innerHTML += '/';
        return true;
    }

    function pushMultiplicationSign() {
        document.getElementById("input-box").innerHTML += '*';
        return true;
    }

    function pushPlusSign() {
        document.getElementById("input-box").innerHTML += '+';
        return true;
    }

    function pushSubtractionSign() {
        document.getElementById("input-box").innerHTML += '-';
        return true;
    }

    function pushAdditionSign() {
        document.getElementById("input-box").innerHTML += '+';
        return true;
    }

    function clearEntry() {
        var id = document.getElementById("input-box");
        var value = id.value;
        value = value.substring(0, value.length - 1);
        id.innerHTML = value;
    }

    function allClear() {
        document.getElementById("input-box").innerHTML = "";
    }

    function calculate() {
        var id = document.getElementById("input-box");
        var entry = document.getElementById("input-box").value;
        var answer = eval(entry);
        console.log(answer);
        id.innerHTML = answer;
    }

### Explanation:

So basically what I did, created push functions for each button or key and appends them on the my calculators screen, for example if key:'1' is clicked the **pushOne()** function adds the number "1" to my screen (text/input box).
For the equal-sign key I created a function called calculate because equals always returns final calculation or evaluated value, the **function caluculate()** takes the string or text from my-screen or input-box which i stored in a variable named entry, using javascript's built-in function **"eval()"** I added the entry as a parameter as in "eval()" to calculate whatever thats from the input-box.

#### eval()
eval() is a function property of the global object.

The argument of the eval() function is a string. 
If the string represents an expression, eval() evaluates the expression.
If the argument represents one or more JavaScript statements, 
eval() evaluates the statements. 
Do not call eval() to evaluate an arithmetic expression; 
JavaScript evaluates arithmetic expressions automatically.

If you construct an arithmetic expression as a string, 
you can use eval() to evaluate it at a later time. 
For example, suppose you have a variable x. 
You can postpone evaluation of an expression involving x 
by assigning the string value of the expression, say "3 * x + 2", 
to a variable, and then calling eval() at a later point in your script.

If the argument of eval() is not a string, 
eval() returns the argument unchanged. 



## Conclusion