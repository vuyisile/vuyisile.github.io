---
Layout:
Title: 
Date:
---

# Everything Be True.

## Overview

In JavaScript, a truthy value is a value that is considered true when evaluated in a Boolean context. 
All values are truthy unless they are defined as falsy (i.e., except for false , 0 , "" , null , undefined , and NaN ). 
JavaScript uses type coercion in Boolean contexts.

## Instruction

Check if the predicate (second argument) is truthy on all elements of a collection (first argument).

Remember, you can access object properties through either dot notation or [] notation.


## My approach

So, a function titled truthCheck which accepted an array of objects (**collection**) and **pre** (the key to check valid). 
Inside the function, I created for loop to access each object which I stored in a new variable that I named valAtIndex. 
Then created a conditional statement that check valAtIndex's value same as pre is a valid, if it is not return false, else return true. 

## Code

    function truthCheck(collection, pre) {
    // Is everyone being true?
        for(var i in collection){
            var valAtIndex = collection[i];
            if(!valAtIndex[pre]){
            return false;
            }
        }
        return true;
    }

    truthCheck([{"user": "Tinky-Winky", "sex": "male"}, 
    {"user": "Dipsy"}, {"user": "Laa-Laa", "sex": "female"}, 
    {"user": "Po", "sex": "female"}], "sex");