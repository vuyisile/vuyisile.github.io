---
layout  :
title   : The Weather Machine
date    : 2017-10-31
---

# The Local Weather Machine.

The local weather machine is a application that generates weather based on the position of a user (meaning that the longitude and latitude are detected).
This was kind of simple to solve because i had a good reliable api and I had an idea of JSON and $.ajax.

### Show the Local Weather 

    Objective: Build a CodePen.io app that is functionally similar to this: http://codepen.io/FreeCodeCamp/full/bELRjV.
    Rule #1: Don't look at the example project's code. Figure it out for yourself.
    Rule #2: Fulfill the below user stories. Use whichever libraries or APIs you need. Give it your own personal style.
    User Story: I can see the weather in my current location.
    User Story: I can see a different icon or background image (e.g. snowy mountain, hot desert) depending on the weather.
    User Story: I can push a button to toggle between Fahrenheit and Celsius.
    Note: Many internet browsers now require an HTTP Secure (https://) connection to obtain a user's locale via HTML5 Geolocation. 
    For this reason, we recommend using HTML5 Geolocation to get user location and then use the freeCodeCamp Weather API https://fcc-weather-api.glitch.me which uses an HTTP Secure connection for the weather. Also, be sure to connect to CodePen.io via https://.
    Remember to use Read-Search-Ask if you get stuck.
    When you are finished, click the "I've completed this challenge" button and include a link to your CodePen.
  
### My Approach.

1. I created two variables called long = longitude and lati = latitude, which when both combind give you the geo-graphical position of something.
2. I created a function and with in the function i a used $.ajax(), where i used "https://fcc-weather-api.glitch.me/api/current?lat=" + **lati** + "&lon=" + **long** as my api
    to return the data based on the position detected by **navigator.geolocation.getCurrentPosition** in JSON format.
3. From the data I took specific or necessary information needed (the icons, temperature,wind speed and humility) and put it on a **document.ready** function so that the data is automatically displayed on the window. 
4. I created an html button that converts from Celsius to Fahrenheit, where used the mathematic or scientific formula to calculate(convert) to Fahrenheit.