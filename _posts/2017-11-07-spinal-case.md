---
Layout  :
Title   : Spinal Case
Date    : 2017-11-07
---

# Spinal Case

## Overview
In my jerny so far I have been learning about ways of naming files (in addition javascript variables and functions), I have learned about camel casing, and funny that I've been using another type of writing called spinal case, which I did not know what it is called. I am not sure the way I describe or define it is good or accrate, but I think that spinal case is a type of writing where all words are lower case and divided by dashes('-'), no spaces in between.

## Problem to solve:
 
In free code camp, I was given a task to create a function that has parameter *(str)* which is a variable that contains a string that I had to convert to spinal case and all alphabets in that should be lower case.
example: "This is spinal case" should change to "this-is-spinal-case".

At first in mind, I had already thought of a way to solve this problem. What I did was split the string by white-spaces ,which returned an array and i looped through it and accessed every word (array[i]) and then I replace every first letter that is in upper case with its lower case form, then i joined the array by dashes ('-'). The good news is that it worked but for one type of situation, example: "This is spinal case".

As I was checking the examples of situations at hand, I had a string that looks like this: "thisIsSplinalTap" and "A_Spinal_Tap_Is". This where I faced a challenge, so when Theo came and told me about regex match and asked me about the rules about or of the problem, I started by highlighting them.

The first rule is that all letters must be lower case, I worked on a situation like this - "thisIsSplinalTap", so to solve that I used the javascript's built in function .replace() which i used to separate the words by spaces replacing the position of regex = /([a-z])([A-Z])/g, in code form it looked like this - str.replace(/([a-z])([A-Z])/g,"$1 $2") after that I used another javascript function .toLowerCase() which change all of the text in str to lower case.

Finally I worked on situations where I have symblos like underscore, example: "a_spinal_tap_is", which I also used .replace() to change /\s+|_/g to dashes.