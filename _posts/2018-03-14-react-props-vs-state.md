---
Layout: 
Title:  "Props vs State"
Date:   2018-03-14
---

# Stateful vs Stateless

## Overview 

* Stateful components are classes that have the ability to be changed (mutable), a state is initialized in the constructor.

* Stateless components are classes that don't have a state which can be considered as props on the DOM, they are not mutable.

## what is a state?

A state is can object that is owned by the component where it is decleared. Its scope is limited to the current component, then that component can update its state whenever necessary if initialize. 

A state is used for internal communication inside a component, and also a state of the parent component usually ends up being props of a child component, when the state is passed out of the current scope, it is refered to as prop.  


## what is a prop?

From what i have seen, a prop is read-only data because it is immutable (unchangable), I consider it as data that is parsed into a component, that component cannot change that property but can use that property.


