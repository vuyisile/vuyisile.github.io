---
Layout:
Title:  Basic Calculator
Date:   2018-01-22
---

# Basic Calculator

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

    
## Conclusion