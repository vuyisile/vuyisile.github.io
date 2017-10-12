
ES6 Arrow Functions: The New Fat & Concise Syntax in JavaScript
Related Topics:
Programming
JavaScript
Business
WordPress
Web
More...

For a high-quality, in-depth introduction to ES6, you can’t go past Canadian full-stack developer Wes Bos. Try his course here, and use the code SITEPOINT to get 25% off and to help support SitePoint.

This article is part of a web development series from Microsoft. Thank you for supporting the partners who make SitePoint possible.

Arrow functions are a new ES6 syntax for writing JavaScript functions. They will save developers time and simplify function scope. Surveys show they are the most popular ES6 feature:

Axel Rauschmayer survey on favorite ES6 features

Source: Axel Rauschmayer survey on favorite ES6 features

Ponyfoo’s survey on the most commonly used ES6 features

Source: Ponyfoo’s survey on the most commonly used ES6 features

The good news is that many major modern browsers support the use of arrow functions.

This post will cover the details of Arrow functions, specifically, how to use them, common syntaxes, common use cases, and gotchas/pitfalls.
What Are Arrow Functions?

Arrow functions – also called “fat arrow” functions, from CoffeeScript (a transcompiled language) are a more concise syntax for writing function expressions. They utilize a new token, =>, that looks like a fat arrow. Arrow functions are anonymous and change the way this binds in functions.

Arrow functions make our code more concise, and simplify function scoping and the this keyword. They are one-line mini functions which work much like Lambdas in other languages like C# or Python. (See also lambdas in JavaScript). By using arrow function we avoid having to type the function keyword, return keyword (it’s implicit in arrow functions), and curly brackets.
Using Arrow Functions

There are a variety of syntaxes available in arrow functions. EcmaScript.org has a thorough list of the syntaxes and so does MDN. We’ll cover the common ones here to get you started.
Let’s compare how ES5 code with function expressions can now be written in ES6 using arrow functions.
Basic Syntax with Multiple Parameters (from MDN)

Basic Syntax with Multiple Parameters

Code Example: http://codepen.io/DevelopIntelligenceBoulder/pen/wMdPoj?editors=101

The arrow function example above allows a developer to accomplish the same result with fewer lines of code and approximately half of the typing.

Curly brackets are not required if only one expression is present. The preceding example could also be written as:

var multiply = (x, y) => x*y;

Basic Syntax with One Parameter

Parentheses are optional when only one parameter is present

Basic Syntax with One Parameter

http://codepen.io/DevelopIntelligenceBoulder/pen/PZmOWQ?editors=101
No Parameters

Parentheses are required when no parameters are present.

No Parameters

Code Example: http://codepen.io/DevelopIntelligenceBoulder/pen/GomOWO?editors=101
Object Literal Syntax

Arrow functions, like function expressions, can be used to return an object literal expression. The only caveat is that the body needs to be wrapped in parentheses, in order to distinguish between a block and an object (both of which use curly brackets).

Object Literal Syntax

Code example: http://codepen.io/DevelopIntelligenceBoulder/pen/zrwPwx?editors=101
Use Cases for Arrow Functions

Now that we’ve covered the basic syntaxes, let’s get into how arrow functions are used.

One common use case for arrow functions is array manipulations and the like. It’s common that you’ll need to map or reduce an array. Take this simple array of objects:


varsmartPhones = [
    { name:'iphone', price:649 },
    { name:'Galaxy S6', price:576 },
    { name:'Galaxy Note 5', price:489 }
];

We could create an array of objects with just the names or prices by doing this in ES5:


// ES5
console.log(smartPhones.map(
    function(smartPhone) {
    returnsmartPhone.price;
    }
)); // [649, 576, 489]

An arrow function is more concise and easier to read:


// ES6
console.log(smartPhones.map(
    smartPhone=&gt;smartPhone.price
)); // [649, 576, 489]

Code Example: http://codepen.io/DevelopIntelligenceBoulder/pen/jWmamX?editors=101

Here’s another example using the array filter method:

Array filter method example

Code Example: http://codepen.io/DevelopIntelligenceBoulder/pen/RrVjgL?editors=101
Promises and Callbacks

Code that makes use of asynchronous callbacks or promises often contains a great deal of function and return keywords. When using promises, these function expressions will be used for chaining. Here’s a simple example of chaining promises from the MSDN docs:


// ES5
aAsync().then(function() {
    returnbAsync();
}).then(function() {
    returncAsync();
}).done(function() {
    finish();
});

This code is simplified, and arguably easier to read using arrow functions:


// ES6
aAsync().then(() =&gt; bAsync()).then(() =&gt; cAsync()).done(() =&gt; finish);

Arrow functions should similarly simplify callback-laden NodeJS code.

What’s the meaning of this?!

The other benefit of using arrow functions with promises/callbacks is that it reduces the confusion surrounding the this keyword. In code with multiple nested functions, it can be difficult to keep track of and remember to bind the correct this context. In ES5, you can use workarounds like the .bind method (which is slow) or creating a closure using var self = this;.

Because arrow functions allow you to retain the scope of the caller inside the function, you don’t need to create self = this closures or use bind.

Developer Jack Franklin provides an excellent practical example of using the arrow function lexical this to simplify a promise:

Without Arrow functions, the promise code needs to be written something like this:


// ES5
API.prototype.get = function(resource) {
    var self = this;
    return new Promise(function(resolve, reject) {
        http.get(self.uri + resource, function(data) {
            resolve(data);
          });
    });
};

Using an arrow function, the same result can be achieved more concisely and clearly:


// ES6
API.prototype.get = function(resource) {
    return new Promise((resolve, reject) =&gt; {
        http.get(this.uri + resource, function(data) {
            resolve(data);
         });
       });
};

You can use function expressions if you need a dynamic this and arrow functions for a lexical this.
Gotchas and Pitfalls of Arrow Functions

The new arrow functions bring a helpful function syntax to ECMAScript, but as with any new feature, they come with their own pitfalls and gotchas.

Kyle Simpson, a JavaScript developer and writer, felt there were enough pitfalls with Arrow Functions to warrant this flow chart when deciding to use them. He argues there are too many confusing rules/syntaxes with arrow functions. Others have suggested that using arrow functions saves typing but ultimately makes code more difficult to read. All those function and return statements might make it easier to read multiple nested functions or just function expressions in general.

Developer opinions vary on just about everything, including arrow functions. For the sake of brevity, here are a couple things you need to watch out for when using arrow functions.
More about this

As was mentioned previously, the this keyword works differently in arrow functions. The methods call(), apply(), and bind() will not change the value of this in arrow functions. (In fact, the value of this inside of a function simply can’t be changed–it will be the same value as when the function was called.) If you need to bind to a different value, you’ll need to use a function expression.
Constructors

Arrow functions cannot be used as constructors as other functions can. Don’t use them to create similar objects as you would with other functions. If you attempt to use new with an arrow function, it will throw an error. Arrow functions, like built-in functions (aka methods), don’t have a prototype property or other internal methods. Because constructors are generally used to create classlike objects in JavaScript, you should use the new ES6 classes instead.
Generators

Arrow functions are designed to be lightweight and cannot be used as generators. Using the yield keyword in ES6 will throw an error. Use ES6 generators instead.
Arguments object

Arrow functions do not have the local variable arguments as do other functions. The arguments object is an array-like object that allows developers to dynamically discover and access a function’s arguments. This is helpful because JavaScript functions can take an unlimited number of arguments. Arrow functions do not have this object.
How Much Use Is There for Arrow Functions?

Arrow functions have been called one of the quickest wins with ES6. Developer Lars Schöning lays out how his team decided where to use arrow functions:

    Use function in the global scope and for Object.prototype properties.
    Use class for object constructors.
    Use => everywhere else.

Arrow functions, like let and const, will likely become the default functions unless function expressions or declarations are necessary. To get a sense for how much arrow functions can be used, Kevin Smith, counted function expressions in various popular libraries/frameworks and found that roughly 55% of function expressions would be candidates for arrow functions.

Arrow functions are here (c’mon Safari!)–they are powerful, concise, and developers love them. Perhaps it’s time for you to start using them!
More Hands-on with Web Development

This article is part of the web development series from Microsoft and DevelopIntelligence on practical JavaScript learning, open source projects, and interoperability best practices including Microsoft Edge browser and the new EdgeHTML rendering engine. DevelopIntelligence offers instructor-led JavaScript Training, AngularJS Training and other Web Development Training for technical teams and organizations.

We encourage you to test across browsers and devices including Microsoft Edge – the default browser for Windows 10 – with free tools on dev.microsoftedge.com:

    Scan your site for out-of-date libraries, layout issues, and accessibility
    Download free virtual machines for Mac, Linux, and Windows
    Check Web Platform status across browsers including the Microsoft Edge roadmap
    Remotely test for Microsoft Edge on your own device

More in-depth learning from our engineers and evangelists:

    Interoperability best practices (series):
        How to avoid Browser Detection
        Using CSS Prefix best practices
        Keeping your JS frameworks & libs updated
        Building plug-in free web experiences
    Coding Lab on GitHub: Cross-browser testing and best practices
    Woah, I can test Edge & IE on a Mac & Linux! (from Rey Bango)
    Advancing JavaScript without Breaking the Web (from Christian Heilmann)
    Unleash 3D rendering with WebGL (from David Catuhe)
    Hosted web apps and web platform innovations (from Kiril Seksenov)

Our community open source projects:

    vorlon.JS (cross-device remote JavaScript testing)
    manifoldJS (deploy cross-platform hosted web apps)
    babylonJS (3D graphics made easy)

More free tools and back-end web dev stuff:

    Visual Studio Code (lightweight code-editor for Mac, Linux, or Windows)
    Visual Studio Dev Essentials (free, subscription-based training and cloud benefits)
    Code with node.JS with trial on Azure Cloud

