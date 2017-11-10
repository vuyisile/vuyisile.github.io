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
and my previous value is equals 0. Then I decleared a new variable that holds the results as in form of a list, where I store my current value.

From there, the idea is to make the current value and the previous value change until it reaches the given input(4) which will be our limit starting from the current value which is equals to 1. In order to make the the current value increase or change wrote [currentValue = currentValue + previousValue] and for previous value I wrote [previousValue = currentValue - previousValue], and result will alway append currentValue [result += currentValue].

The next step was to make result exclude all even number, I had a loop that iterates to the limite of the given input [while(currentValue <= Input)] and inside the loop I had a conditional statement that check if currentValue is divisible by 2 but the remainder is not 0 [if(currentValue%2 !== 0)], then I moved result in side the conditional statement.

After that, I created a new variable called sum which is equals 0 and a new loop that will iterate through result (for(var i in result), in side the loop I added every element or number in result [sum += result[i]], and finally I returned sum.
