---
Layout:
Title:
Date:
---

# Sum all Odd Fibonacci numbers.

## Overview

After doing a research about Fibonacci number, in order to get more knowledge about what they are, 
According to Wikipedia Fibonacci numbers are defined as numbers characterized by the fact that every number after the first two is the sum of the two preceding ones:
1 , 1 , 2 , 3 , 5 , 8 , 13 , 21 , 34 , 55 , 89 , 144 , …

Often, especially in modern usage, the sequence is extended by one more initial term: 0 , 1 , 1 , 2 , 3 , 5 , 8 , 13 , 21 , 34 , 55 , 89 , 144 , …

The Fibonacci spiral: an approximation of the golden spiral created by drawing circular arcs connecting the opposite corners of squares in the Fibonacci tiling;
this one uses squares of sizes 1, 1, 2, 3, 5, 8, 13 and 21.By definition, the first two numbers in the Fibonacci sequence are either 1 and 1, or 0 and 1, depending on the chosen starting point of the sequence, 
and each subsequent number is the sum of the previous two.The sequence Fn of Fibonacci numbers is defined by the recurrence relation: F n = F n − 1 + F n − 2 with seed values,F 1 = 1 , F 2 = 1 or  F 0 = 0 , F 1 = 1. 


# My approach. 

Now that I have an idea of what they are and given the example of how the sequence is determined which is:F 1 = 1 , F 2 = 1;
I wrote my algorithm in psudo code if given 4 as an input.
Therefore this how i presented it in my note book:

I imagined I have 2 variables one that holds the current value and another that holds the previous value. My current value is equals to 1 and less that the given input (4),
and my previous value is equals 0. then I decleared a new variable that holds the results as in form of a list.

From there, if
