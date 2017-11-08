---
Layout:
Title:	Arrow Functions
Date:	2017-10-10
---
### Arrow functions.

An arrow function has a shorter syntax than a function expression and does not bind its own this, arguments, super, or new.target. The arrow function expressions are best suited for non-method functions, and they cannot be used as constructors.

Arrow functions can have either a concise body or block body. In a concise body, only an expression is needed, and an implicit return is attached. In a block body, you must use an explicit return statement. e.g concise body : func = x => x * x; block body : func = (x,y) => {return x + y;};
