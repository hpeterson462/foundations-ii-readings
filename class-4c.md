# Articles

## *Asynchronicity in Programming Languages*

* computers are asynchronous by design
* every program runs for specific time slot and then stops execution to let another program continue
* normally programming languages are synchronous - eg: JS
* callback - event handler accepts a function which will be called when event is triggered
* callback - function that passes a value to another function and will only be executed when the event happens
* callback can be used onload or time out
* callbacks great for simple cases, but can become complicated
* promises and async/await are alternatives to callbacks in ES6


## *Understanding JavaScript Promises*

* Promise - proxy for a value that will eventually become available
* once promise called, it will start in pending state
* returned promise is either in resolved state or rejected state
* `new Promise()` constructor with `(resolve, reject)` attributes
* `checkIfItsDone()` will execute promise and wait for it to resolve using `.then` callback - if there's an error it will handle it in `catch` callback
* chaining promises can return one promise and then another
* `Promise.all()` synchronizes different promises
* `Promise.race()` runs as soon as one of the promises resolves and runs attached callback once with the result of the first promise resolved
* if `Uncaught TypeError: undefined` then use `new Promise()` instead of `Promise()`


## *MDN Asynchronous JavaScript*

* Synchronous - only one thing can happen at a time
* 2 types of Asynchronous 
    1) callbacks
    1) promises 
* Callbacks are versatile - allow control of order in which functions are run and what data passes between them
* Promise - object representing completion or failure of async operation
* Promises use event queue - they don't block subsequent JS code from running
* Promises can: 
    * chain multiple async operations together
    * callbacks are always called in strict order they're placed
    * error handling `.catch()`
    * avoid inversion of control
* Problems with callbacks:
    * messy/hard to read
    * `failureCallback()` must be called multiple times
* `Blob()` transforms `fetch()` response of raw body contents into object
* `.then()` creates new promise


## *MDN Using Promises*

* Promise - an object representing the eventual completion or failure of an asynchronous operation
    * can attach callbacks (instead of passing callbacks into function)
* Promise chain
    * `const promise = doSomething();
const promise2 = promise.then(successCallback, failureCallback);
`
* Always return results, otherwise callbacks won't catch the result of a previous promise
* Promise rejected
    * `rejectionhandled` - rejection has been handled by executor's reject function
    * `unhandledrejection` - promise is rejected but there is no rejection handler available
* Mixing old-style callbacks and promises is problematic - nothing catches error
* Functions passed to `.then()` will  never be called synchronously
* Nesting controls structure to limit the scope of `catch` statements


## *JS Promises in 20 Mins*

* JS is a single-thread language
* Vanilla asynchronous callbacks take two functins as arguments
* Old-style callbacks are hard to debug
* Promise takes an executor - a function whose results are controlled asynchronously
* Promise has internal state (which can't access directly)
    * State starts out pending (only once in lifecycle) - no callbacks run
    * Can only change to fulfilled or failure in lifecycle
* Promise has value
* Has to have access to `.then()`
* Promise decides which case to run based on internal state
* Control code functionally


## *JS Promises*

* Somewhat like event listeners except:
    * promise can only succeed or fail once
    * if promise has succeeded or failed, the correct callback will be called even though the event took place earlier
* Promise can be:
    * fulfilled
    * rejected
    * pended
    * settled
* Async code:
    1) start a spinner to indicate loading
    1) fetch some JSON
    1) add title to page
    1) fetch each piece
    1) add to page
    1) stop spinner
* Transform values by returning new value
    * `var promise = new Promise(function(resolve, reject) {
  resolve(1);
});`
* Queue with `.then()` - takes 2 arguments
* `Promise.all` takes an array of promises and creates a promise that fulfills when all successfully complete
    * array of results is in the same order as promises passed in


## *MDN Fetch*

* `fetch()`
    * won't reject HTTP error status
    * can receive cross-site cookies
    * won't send cookies
* controlled by `connect-src` 
* optional second parameter `init` object that allows control of different settings
* will reject with `TypeError` when network error is encountered or CORS is misconfigured on server-side
* `Headers` can be sent in requests and received in responses
* Response objects returned when `fetch()` promises are resolved
* requests and responses may contain body data


## *Fetching Data*

* `fetch()` is the easist way for JS to deal with data from servers
* makes network request to url and returns promise
* promise resolves with response object when remote server responds with headers
* to read response body, must call response method on it - eg: `text()` `json()`
* for every `fetch()` whose data you want to show or manipulate, you need at least 2 `then()` methods:
    1) return response method that retrieves data
    1) works with data

