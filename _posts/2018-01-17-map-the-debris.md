---
Layout:
Title:
Date:
---

# Map-the-debris

## Overview

In this article I will be explaining how I solved the Map-the-debris challenge, which was based on calculating the **orbital period** and from the instructions, 
my function should return a new array with one or more objects, 
that contains a name and the orbital period based on the given average altitude. 

The **orbital period** is the time a given astronomical object takes to complete one orbit around another object, 
and applies in astronomy usually to planets or asteroids orbiting the Sun, moons orbiting planets, 
exoplanets orbiting other stars, or binary stars.


## Instructions

    Return a new array that transforms the element's average altitude into their orbital periods.

    The array will contain objects in the format {name: 'name', avgAlt: avgAlt}.

    You can read about orbital periods on wikipedia.

    The values should be rounded to the nearest whole number. The body being orbited is Earth.

    The radius of the earth is 6367.4447 kilometers, and the GM value of earth is 398600.4418 km3s-2.


# My Approach:

## The Logic:

I given a function with one parameter which is accepted as an array of json, each object has a **name** and an **average altitude**(altAvg). 
I am also given constant values of variables-**GM** and **earthRadius**.




## Code:
    function orbitalPeriod(arr) {
        var newArr = [];
        var orbitalPeriod = 0;
        var GM = 398600.4418;
        var pie = 3.1415926535898;
        var earthRadius = 6367.4447;
        var sum = 0;
        for (var index = 0; index < arr.length; index++) {
            sum = earthRadius + arr[index].avgAlt;
            orbitalPeriod = Math.round((2 * pie) * Math.sqrt(Math.pow(sum,3) / GM));
            newArr.push({ name: arr[index].name, orbitalPeriod: orbitalPeriod });
        }
        return newArr;
    }

    console.log(orbitalPeriod([{ name: "sputnik", avgAlt: 35873.5553 }]));

    console.log(orbitalPeriod([{name: "iss", avgAlt: 413.6}, {name: "hubble", avgAlt: 556.7}, 
    {name: "moon", avgAlt: 378632.553}]));