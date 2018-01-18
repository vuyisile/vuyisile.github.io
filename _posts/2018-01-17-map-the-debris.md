---
Layout:
Title:
Date:
---

# Map-the-debris

## Overview



## Instructions

    Return a new array that transforms the element's average altitude into their orbital periods.

    The array will contain objects in the format {name: 'name', avgAlt: avgAlt}.

    You can read about orbital periods on wikipedia.

    The values should be rounded to the nearest whole number. The body being orbited is Earth.

    The radius of the earth is 6367.4447 kilometers, and the GM value of earth is 398600.4418 km3s-2.


# My Approach

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