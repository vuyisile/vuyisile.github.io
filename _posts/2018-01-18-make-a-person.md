---
Layout:
Title:
Date:
---

# Make a person.

## Overview

I was given this challenge (make-a-person) in free-code-camp,from this challenge I learned about Closures and Details of the object model.

what is a Closure?- It is the combination of a function and the lexical environment within which that function was declared. 
A Lexical Environment is a specification type used to define the association of Identifiers to specific variables and 
functions based upon the lexical nesting structure of ECMAScript code.

Details of the object model- JavaScript is an object-based language based on prototypes, rather than being class-based. Because of this different basis, 
it can be less apparent how JavaScript allows you to create hierarchies of objects and to have inheritance of properties and their values. 


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