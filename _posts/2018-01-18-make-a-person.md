---
Layout:
Title:
Date:
---

# Make a person.

## Overview



## Instructions

Fill in the object constructor with the following methods below:

    getFirstName()
    getLastName()
    getFullName()
    setFirstName(first)
    setLastName(last)
    setFullName(firstAndLast)

Run the tests to see the expected output for each method.

The methods that take an argument must accept only one argument and it has to be a string.

These methods must be the only available means of interacting with the object.


# My Approach

## Code:

    var Person = function(firstAndLast) {
        var firstName ='';
        var lastName = '';
        var currentNames = function(names){
            names = names.split(" ");
            firstName = names[0];
            lastName = names[1];
        return firstName,lastName;
        } ; 
    
        currentNames(firstAndLast);
    
        this.getFullName = function(namesInFull) {
        namesInFull = firstName+ ' ' + lastName;
        return namesInFull;
        };
        this.getFirstName = function(){
        return firstName;
        };
        this.getLastName = function(){
        return lastName;
        };
        this.setFirstName = function(first){
            firstName = first;
            return firstName;
        };
        this.setLastName = function(last){
        lastName = last;
        return lastName;
        };
        this.setFullName = function(fullNames){
        
        return currentNames(fullNames);
        };
        return firstAndLast;
    };

    var bob = new Person('Bob Ross');
    bob.getFullName();

    console.log(Person("Mark Nan"));
    console.log(Person("Vince Rassels"))