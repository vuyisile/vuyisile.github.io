---
Layout:
Title: Translate from Binary to English.
Date: 2017-11-21
---

# Binary Agents.

## Overview

In this article, I will be explain my code or algorithm that I wrote to translate binary codes to english words or sentances. 
In computer science A binary code represents text, computer processor instructions, or other data using any two-symbol system, but often the binary number system's 0 and 1. 
The binary code assigns a pattern of binary digits (bits) to each character. 
For example, a binary string of eight bits can represent any of 256 possible values and can therefore represent a variety of different items.



## Instructions

Return an English translated sentence of the passed binary string.

The binary string will be space separated.

Here are some helpful links:

    String.prototype.charCodeAt()

    String.fromCharCode()



## My approach

I was given a string of binary codes, between all the codes there spaces so in order for me to access each code I had to divide the codes in to an array, so I used the javascript's built in function .split() which if returned will be an array, so I stored that array in a variable that I created called **splittedStr**.
I then accessed every code in "splittedStr" using a for-loop. From there, I declared a new variable titled **translation** (an empty array) that I used in my for-loop to **.push()** in String.fromCharCode(**the binary code**), this the part where I access the character represented by the binary code using the parseInt method to convert the string binary digits to an integer. 
Inside the parseInt method, I used radix, base number of unique digits, including zero, used to represent numbers in a positional numeral system.


## Code

    function binaryAgent(str) {
       var translation = [];
       splittedStr = str.split(' ');
       for (var i in splittedStr){
        translation.push(String.fromCharCode(parseInt(splittedStr[i],2)));
       }

        return translation.join('');
    }

        binaryAgent("01000001 01110010 01100101 01101110 00100111 
        01110100 00100000 01100010 01101111 01101110 01100110 01101001 
        01110010 01100101 01110011 00100000 01100110 01110101 01101110 
        00100001 00111111");

