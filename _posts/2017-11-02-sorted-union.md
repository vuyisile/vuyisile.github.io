---
Layout  :
Title   : The Sorted Union
Date    : 2017-11-02
---

# Sorted Union.

In Free Code Camp, I am currently completeting Intermediate Algorithm Scripting, now focusing on sorted-union, 
task number 267, which i found very challenging but looking at the examples of how the output should be, 
i understood that the function has to combine values that are in the arrays provided as arguments in to one array and the should be no duplicates.

## Details:

-   Write a function that takes two or more arrays and returns a new array of unique values in the order of the original provided arrays.
-   In other words, all values present from all arrays should be included in their original order, but with no duplicates in the final array.
-   The unique numbers should be sorted by their original order, but the final array should not be sorted in numerical order.

## My Logical thinking about this algorithmic problem.

Understanding that algorithm is set of rules to be followed in calculations, by looking at the solutions I attempted to solve the problem but I failed a couple times until I realized that I did not understand the instructions. So I took a step back and re-read the details and I highlighted the key points about this task, therefore I broke them down for simplicity and did one thing at a time.

As I was highlighting the keys of this problem, the first instruction said I must write a function that takes two or more arrays,
from this statement I understood that the function's arguments are unlimited so the plan is to create a variable that **creates an array of arguments** passed in the funtion when executed. I moved on to the second bit of the instruction which states that the function should return a **new array**, in this case I knew I had to create another variable of an empty array (var combo = []), where I will store the all the values from the arrays passed as arguments after iteration. After I all that process, my final array still has duplicates and I realized that in the instructions it was stated that there should be **no duplicates**, I had to compare the values in the final array so that if the array contains values that are the same or repeated, only one of each is left. The last instruction is that the unique numbers should in the original order, so I left the final array unsorted.


## Explanation of my approach in code.


-   The function was already created for me, so I went to the second step- I created a variable **var argsArr = Array.from(arguments);** because the        arrays could be *two or more*.
-   Then I created **var combo = [];** to store the values from all arrays.
-   From there I loop through the **argsArr** to access all arrays and stored the values in a new variable, **var valOfIndex = argsArr[i];**,
-   Which I looped through to access all the numbers within each array, then I pushed the numbers in *"combo"* **combo.push(valOfIndex[n]);** and the       output looked like this:**[1, 2, 3, 5, 2, 1, 4, 2, 1, 6, 7, 8]**.
-   Lastly, I used the filter method to compare and remove duplicates and stored it in a new variable called **result** and returned it after:
    ***var result = combo.filter(function(value1,value2){ return combo.indexOf(value1) === value2;}) return result;***

## Conclusion.

As I said, I found the problem challenging and because I did not read to understand the question in the first place, so from this problem I've learnt that I have to a logical memory of the steps to solve any challenge like this one, so rule number one about solvin a problem is to break down the details and attempt the solving the problem bit-by-bit.
