---
Layout:
Title: Smallest common multiple (the solution)
Date: 2017-11-15
---

## Rules of this problem.

-   Find the smallest common multiple of the provided parameters that can be evenly divided by both, as well as by all sequential numbers in the range between these parameters.

-   The range will be an array of two numbers that will not necessarily be in numerical order. 
    e.g. for 1 and 3 - find the smallest common multiple of both 1 and 3 that is evenly divisible by all numbers between 1 and 3.



## My approach

Firstly, I created a function titled **findSmallestMultiple** that accepts an array as an argument. Knowing the given the rule that the range will be in an array of two numbers that will not necessarily be in numerical order, I created two variables on called **min** that contains the lowest number in the array and the other called **max** contains the hightest number in the array, then I created a new variable called **currentMultiple** which contained **max**.

From there I created a function titled **checkIfMultiple** that accepted three arguments, first paramtere being **cm** for **currentMultiple**, second being **min** for **minimum value** and last being **max** for **maximum value**. Within the function I created a for Loop that took the **min** variable as a beggining point and incremented it by one until it reaches the same number as the **max value**. I had a condition in that for loop that checks if the currentMultiple is divisible by **i** which is equal to **min** and returns false if the remainder is not 0, otherwise returns true.


There after, outside the **checkIfMultiple** function but inside **findSmallestMultiple**, I created a while loop that checks the condition of **checkIfMultiple** if the function's result is not true then **currentMultiple** should increment by **max**.

