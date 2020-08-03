# Articles

## *MDN Template Literals*

* Enclosed in backtics and dollar sign/curly braces syntax used for variables ``${}``
* Example: `Fifteen is ${a + b} and not ${2 * a + b};`
* Tags used to parse template literals with a function
    * Example: `function myTag(strings, personExp, ageExp){}`
    * Tag functions don't need return string
* Raw property is available on first argument of tag function that allows you to access raw strings as they were entered without escape sequences
    * String.raw() method
    * Example: `function tag(string.raw[0]);`

## *Getting Literal with ES6 Template Strings*

* Template literals allow for better:
    * String interpolation
    * Embedded expressions
    * Multiline string without hacks
    * String formatting
    * String tagging for safe HTML escaping, localization, etc.
    * Example: ``Hello ${name}!``
* Tagged Templates:
    * `function(["Hello ", "!], you, adj);`

## *CSS Tricks - Template Literals*

* Single line:
    * `let newString = `A string`;`
* Multi-line: 
    * `let multiLineString = `Yay!`;`
* Expressions:
    * `let name = `Hi my name is ${name}`;`
* Evaluate expressions:
    * `let total = `The price is ${price * tax}`;`
* Data structures in HTML:
    * `return `<h3>${data.name}</h2>``
* Tagged Templates:
    * call function with backtics
    * `taggedLiteral `test``
* Reusable Templates:
    * `const studentTemplate = student`<h2>${name}</h2> is a student`;`
    * Rest parameter: `...key`
        * gathers any parameters the function has and create an array
        * `const student = function(strings, ...keys){};`

## MDN forEach()*

* executes a function once for each array element
    * `array.forEach(callback(currentValue[, index [, array]])[, thisArg]);`
* callback needs three arguments:
    1) value of element
    1) index of element
    1) array object being traversed
* Example: 
    * `array.forEach((element) => {numCallbackRuns++});`
* convert a for loop:
    * before: `for(let i = 0; i < items.length; i++){copyItems.push(items[i])}`
    * after: `items.forEach(function(item){copyItems.push(items){copyItems.push(item)})`

## *For vs forEach()*

* `for (var i = 0; i < arr.length; i++) {
  console.log('Element', i, 'is', arr[i]);
}` =equals= `arr.forEach(function(element, i) {
  console.log('Element', i, 'is', element);
});`

