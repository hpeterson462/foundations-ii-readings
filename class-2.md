# Articles

## *Applying Atomic Design*

* Atoms included basic HTML elements like labels, inputs, buttons, etc.
* Split page into sections - organisms, molecules, and atoms
* With React multiple files, create smallest section first and work your way up - doesn't duplicate code
* Designing systems of components in React


## *Thinking in React*

* Single resopnsibility principle - a component should only do one thing
*  Idenitfy components in mock, then arrange them into a hierarchy
* Props are a way to pass data from parent to child
* React is one way data flow (one way binding)
* Two types of model data: props and state
* Think of the minimal set of mutable state the app needs - DRY code (don't repeat yourself)
* Three questions to ask to figure out which one is state:
    1) Is it passed from parent to child via props?
    1) Does it remain unchanged over time?
    1) Can you compute it based on any other state or props in the component?
* For each piece of state in the app:
    * Identify every component that renders something based on that state
    * Find a common owner component 
    * Either the common owner or another component higher up in the hierarchy should own state
    * If you can't find a component where it makes sense to own the state, create a new component solely for holding the state and add it somewhere in the hierarchy above the common owner component


## *UI Components by Design*

* Two types of components: 
    1) Foundation components - primary expression of design; defining parts of the experience
    1) Application components - part of larger scope composed of one of more Foundations components
* Work flow - 
    1) learn
    1) design
    1) isolate
    1) elaborate
    1) build
    1) integrate
* Break app down into component parts
* Isolate core UI elements so they can elaborate on their structure, appearance, and behaviors


## *Callbacks in Javascript*

* Callback - a function that is executed after another function (normally asynchronous)
* Higher-order functions - functions are objects and can take other functions as arguments
* JS will keep executing while listening for events
* When using API, callbacks necessary while waiting for response from server


## *JS Callback Functions*

* First argument in function are assigned to first variable
* Function one variable can be passed to be used as argument in function two
* Functions can be used as arguments inside other functions
* Callback - a piece of executable code that is passed as an argument to other code that is invoked at sometime
* No limit to number of callbacks of a function
* Can pass as many callbacks to another function as needed
* Callbacks used synchronously or asynchronously 


## *MDN First-class Function*

* A programming language has first-class functions when those functions can be treated like a variable
* Function can be passed as an argument
* Can return a function
* Double parentheses to invoke callback and return functions


## *MDN Callback Function*

* Function passed into another function as an argument
* `.then()` used in asychronous callbacks


## *JS Classes*

* `class MyClass {constructor()}`
    * creates the function MyClass
    * stores class methods in MyClass.prototype
* Classes may include getters and setters
* `this` points to object containing it


## *Intro to Object-Oriented Programming*

* OOP
* Class - a set or category of things that have the same property or attribute in common
* An object is an instance of a class
    * can create many objects with same class
* Classes are often related to inheritance
    `extends`
* Create an object from a class using `new`
* Defining class:
    * simple syntax to declare
    * simple way to access current instance
    * simple syntax to extend
    * simple access super class
    * simple way of telling if an object is an instance of a particular class
* Functional programming uses `bind`, `call` and `apply`


## *Object Methods*

* Objects represent real world entities and act on something real
    * user and shopping cart
* To access an object `this` keyword used
    * value of `this` is object before the dot
* If `this` is inside a function, JS expects it to be called in an object
* Arrow functions have no `this`
    * used from outer function or object
* Methods - functions stored in objects 
    * allow objects to at like `object.doSomething`
    * can reference object as `this`
* `this` has defined run time
    * has no value until function is called
    * has the value of the object when being called

