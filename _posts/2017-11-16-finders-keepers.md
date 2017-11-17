---
Layout:
Title: Solving the Finders-Keepers problem
Date: 2017-11-16
---

# Finders-Keepers.

## Overview.

Finders Keepers is an english idiom, derived from an old children's adage "finders keepers, losers weepers",which basically asserts that anything found or discovered by someone automatically entitles them to ownership of that property. Understanding the definiton in life terms this task was easy to complete.

## My Approach. 

I created a function titled findElement, inside the function I declared a variable filteredArr where I applied the javascript's built in function called filter. Not forgetting that the function has a parameter named arr and another function as parameter that returns a numbers that are divisible by 2. for my solution I used the filtered out numbers that are divisible by 2, which is an array stored in filteredArr, then from that array I took the first value at index 0 and returned it because the it is always the first item considering the definition of Finders-Keepers.

### Solution.
<!-- function findElement(arr, func) {
  var num = 0;
  var filteredArr = arr.filter(func);
  return filteredArr[0];
} -->