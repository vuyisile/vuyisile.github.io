---
Layout:
Title: Solving The Steam-roll Array.
Date:  2017-11-20
---

# The Steamroller.

## Overview

I was completing this free-code-camp challenge, which I had difficulties solving it because I did not understanding what a steam roller is, so I went and look-up on what it is.
According to Wikipedia, A steam roller a type of heavy construction machinery used for leveling surfaces or flattening the surface.

Steamroller, from the given test example I noticed that I have nested arrays in an array, so my job is to extract the values inside the nested arrays, leveling them down together to one chatter. This means my function should accept an array of nested arrays. 


## Instructions

Flatten a nested array. You must account for varying levels of nesting.


## My approach

For my solution I used the recursion method, where the solution to a problem depends on solutions to smaller instances of the same problem (as opposed to iteration).
So, a function titled **steamrollArray** was declared for me which had a parameter called **arr**, I started checking for necessary tools to use to complete this problem, a for-loop, and empty array structure, isArray() and concat().

I created a variable named final (my empty array), then a for-loop to Iterate through **arr**, in side my loop i created a conditional statement that will allow me to push a values inside **final** if it is not an **Array** (**if(Array.isArray(arr[i]) === false)**),else if it is an Array iterate again (**final = final.concat(steamrollArray(arr[i]));**)
,this is the part where I used recursion (for nested arrays), outside the conditional statements I returned **final**.


## Code

        function steamrollArray(arr) {
        // I'm a steamroller, baby
            var final = [];

            for(var i = 0; i < arr.length; i++){
                if(Array.isArray(arr[i]) === false){
                final.push(arr[i]);
                }else{
                final = final.concat(steamrollArray(arr[i]));
            
                }
            
        }

        return final;

        }
        steamrollArray([[["a",1]], [["b"]]]);


## Conclusion

In solving this problem I have learnt about recursion and its power to destory or ease complexity, now I know where or when to use it as a tool because it is incredible.
