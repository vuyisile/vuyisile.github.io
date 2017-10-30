---
layout  :
title   : My approach on the random quote machine.
date    : 2017-10-27
---

### The Random Quote Machine.

In FreeCodeCamp I completed challenges under the ***JSON APIs and AJAX***, where I was learning how to get requests and diplay the reponse on canvas. 
After those challenges, I was given the Random Quote Machine project to solved based on the JSON APIs and AJAX topic.

## Instructions given.

Create a Random Quote Machine, that gets or generate a new random quote from an API and display on the window with just a click of a button.
- It should have a "Get New Quote" button.
- And a "Twitte" button which alows a the user to twitte the current quote. 

## The general logic based on the problem.

- I need to first find reliable API.
- I need get the nessessary infomation.
- I need a "New Quote" button.
- I need a "Twitte" button.
- Display the new quote using the "New Quote" button.
- Get the "Twitte" button post the current quote requested.

## My approache.

- First, knowing the structure of ajax and json from the previous challenges I created a function that requests an object in json format using the  
"https://api.forismatic.com/api/1.0/" url and return the response (which is in json format).

- Secondly, I created a function for the "New Quote" button, that gets the information that I needed from the response (of the json request) and display it on the window.

- Lastly, I created a "Twitte" button, which takes the currently viewed quote and enables the user to tweet it to their account.