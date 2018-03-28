---
Layout: 
Title:  "Learning React"
Date:   2018-03-12
---

# Learning React-js

## Overview

What is React?... React is a library created for building Front-end (User Interface), it is considered as the most flexible, efficient and declarative framework for rendering HTML through javascript using its Components.

## React Components

I did a bit of reading about Components and according to my understanding,they are tools that I can use to instruct react to render or express whatever I want, with efficiency that React carries, it updates and renders the right components when my data changes.

A component takes in parameters called props, and returns a hierarchy of views to display via the render method. The render method returns a discription of whatever I want to render on the screen or the DOM.

* In javascript classes (react components), it's  required that  a method called super() is used when defining a constructor of sub-classes.

* In order to update a component (that has a state), it is required that this.setState() is called so that React merges the passed state and re-renders the updated component along with its dessendants.

## Creating a React Component or Class (Syntax)

### The old way of creating a Class:

    React.createClass(){
     render(){
         return(
             <h1>Hello World!</h1>
         )
     }
    }

### The New way of creating a Class:

    Class App extends React.Component{
        render(){
         return(
             <h1>Hello World!</h1>
         )
     }
    }


## Conclusion 

Components are self-sustaining, Independent micro-entites that describe a part of a UI (User Interface).
and I believe that react can be really usefull because it offers the use of reusable components 
which can make programming quite simple.
