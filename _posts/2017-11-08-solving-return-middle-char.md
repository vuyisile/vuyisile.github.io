---
Layout:
Title: Finding the middle Character
Date:
---

# Finding the middle Charactor

In a task given to me by free code camp to find the middle charecter of a string, I had to create an algorithm that would solve the challenge given at hand.

## creating the algorithm

 -   the challenge in solving the problem was that, to be able to access the middile character, first I had to determine the length of the string there by using the javascript built in function called .length().
 -   now that I have determined the length, I can use it to find half of the length, that would be used to access the middle character of the string.
 -   the challenge in using the half length to determine the middle character is that :
        -   **Situation 1:** when the length is an **odd number**, half of it will be a decimal number therefore not being a precise number to use as index in order to determine the middle character.
        -   **Situation 2:** when the length is an **even number**, half of it cant be used to determine the middle character, as the even length has two middle characters.

### Situation 1:
    First i declared global variables called indexToUse and finalAnswer.

    where the length is an odd number and when it is divided by 2, returns a decimal. That being so, I created a conditional statement and said If the length is divisible by 2 is greater or equals to 1, inside my if statement i assigned indexToUse to be length/2, then i used the Math.floor to round it down to the nearest whole number, therefore I assigned finalAnswer to string[Math.floor(indexToUse)].

### Situation 2:
    
    where the length is an even number and returns a whole number when divided by 2. That being so, I said else if the length is divisible by 2 and remainder is 0, inside my else-if statement i assigned indexToUse to be length/2, then used indexToUse-1 and indexToUse to access the 2 middile charaters, therefore I assigned finalAnswer to string[indexToUse-1] + string[indexToUse].


