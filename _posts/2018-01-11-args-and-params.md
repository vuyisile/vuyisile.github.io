---
Layout:
Title:  args and params
Date:   2018-01-11
---

# Overview

Hi, this post is based on understanding the difference between Arguments and/or Parameters within a function. I have came across people that use the interchangable when explaining functions, my objective is to make clearity about the two, because I believe we have to use the right words to explain things.


## What are Parameters?

Oh!! this is easy, before I came to that conclusion I did some research,and initially I was told that parameters are variables that (preferably) have no specific value defined for them, so that they can be used for working any values that can be used in the function. In simple english words,parameters are placeholders/ or storage for values that are to be used when exercuting the function. The advatage of using parameters is that it makes it easy for programers to use the function through out the code.


### Example

This is an example of a function that has parameters that are not given default values:

            //this function has two paramenters that multiply together.
            function multiply(num1,num2){
                return num1 * num2
            }


## What are Arguments?

Arguments are basically actual values or data (like arrays, numbers, strings or objects) that are used when the function is exercuted. 

### Example

In this example I am exercuting the function or code that from the parameters explanation with arguments (the actual values);

            console.log(multiply(3,4));
            console.log(multiply(7,9));
            console.log(multiply(3,2));
            console.log(multiply(12,10));