---
Layout:
Title:  Inventory Update
Date:   2018-01-08
---

# Inventory Update

## Overview

According to definition an **inventory** is a complete list of items such as property, goods in stock, or the contents of a building, and **updating** is modernizing.
So by definition **Inventory Update** is something that modernizes a list of items. 

Understanding the definition and the instructions, the Idea of this task is to create a function that accepts two arrays, one being the **currentInventory** and the other being **newInventory**, both Inventories are expected to be in 2D array form.
The function must compare the currentInventory with the newInventory and update the currentInventory by taking or referring from the newInventory. 
In both inventories there is a **number per Item** (inventory = [[10,'spice']]), if the item already exists in the currentInventory and newInventory, 
only numbers from both inventories of the same item must be summed together, else if there is a new Item from the newInventory, 
then it should be added to the currentInventory. 


## Instructions

Compare and update the inventory stored in a 2D array against a second 2D array of a fresh delivery. Update the current existing inventory item quantities (in arr1).
If an item cannot be found, add the new item and quantity into the inventory array. The returned inventory array should be in alphabetical order by item.



# My Approach
## Code
        function updateInventory(arr1, arr2) {
        var con = arr1.concat(arr2);
        var result = [];
        var sum = 0;
        var ref = [];
        var expectedOutput = [];

            for(var i in arr1){
                for(var j in arr2){
                    if(arr1[i][1] === arr2[j][1]){
                    sum = arr1[i][0] + arr2[j][0];
                    result.push([sum,arr2[j][1]]);    
                    }
                }
            }
            con.forEach(function(e){
                var stringed = result.toString();
                if(stringed.indexOf(e[1]) === -1){
                    result.push(e);
                }
            });
            for(var k in result){
                ref.push(result[k][1]);
            }
                ref.sort(alphabetical);
            
            for(var h in ref){
                for(var g in result){
                    if(ref[h] === result[g][1]){
                        expectedOutput.push(result[g]);
                    }
                }
            }
            return expectedOutput;
        }

        //testing arrays.
        var curInv = [
            [21, "Bowling Ball"],
            [2, "Dirty Sock"],
            [1, "Hair Pin"],
            [5, "Microphone"]
        ];
        var newInv = [
            [2, "Hair Pin"],
            [3, "Half-Eaten Apple"],
            [67, "Bowling Ball"],
            [7, "Toothpaste"]
        ];
        updateInventory(curInv, newInv);




