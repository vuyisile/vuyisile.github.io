---
Layout:
Title: Solving the Drop-It challenge
Date: 2017-11-17
---

# Drop-It

## Overview

While I was reading the problem statement I came across similar instructions from the one's in the previous challenge (Finders Keepers) . 
This challenge takes a function as an argument that has to return true.

Reading the code provided code, I've learnt that I have two arguments passed in with the function call:

           dropElements([1, 2, 3], function(n) {return n < 3; });

The first is an array: [1, 2, 3].

The second is a function: [function(n){return n < 3;}.

From the instructions, what I need to do is remove items in the array (arr) until the second argument returns true, then return the rest of the array.

## Problem statement

Drop the elements of an array (first argument), starting from the front, until the predicate (second argument) returns true.

The second argument, func, is a function you'll use to test the first elements of the array to decide if you should drop it or not.

Return the rest of the array, otherwise return an empty array.

        <--
        function dropElements(arr, func) {
             // Drop them elements.
             return arr;
        }

         dropElements([1, 2, 3], function(n) {return n < 3; });
        -->


## My Approach

First, I created a variable called **len**, where I stored the length of the given array (**arr**) ,and another variable called **m** (for measurement until equals len) which I initialized it to be 0. 
From there, I then created a while loop to compared my **len** with **m**, where [m < len], inside my while loop I had a conditional statement to chech if each element is not > or = 3 (when the function [func] returns false for the number at index 0), whenever the func returns false, I shift or delete the number at position 0 using the javascript built in funtion ***Array.prototype.shift()*** else if the number at index 0 is true **break** (this means the func returned true because the element at 0 is > or = 3).

   ### Solution in Code form.

        <!-- 
            function dropElements(arr, func) {
                // Drop them elements.
                 var len = arr.length;
                 var m = 0;
                 while(m < len){
    
                    if(!func(arr[0])){
                        arr.shift();
                    }else{
                        break;
                    }
    
                    m++;
                }
  
                return arr;
            }

            dropElements([1, 2, 3, 7, 4], function(n) {return n >= 3; }); 
            -->