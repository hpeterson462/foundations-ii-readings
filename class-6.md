# Articles 

## *What is Node and When Should I Use It?*

* "Node.js is an event-based, non-blocking, asynchronous I/O runtime that uses Google's V8 JS engine and libuv library."
* Built on Google Chrome's V8 JS Engine
    * V8 engine - open source JS engine that runs in Google Chrome (including Brave, Opera, and Vivaldi)
    * Compiles JS directly to native machine code that your computer can execute
    * Node.js executed in local computers
* How to Install
    * use version manager to install
    * check that Node.js is installed by typing `node -v` into terminal
* NPM - JS Package Manager
    * install globally using `npm install -g jshint` command
    * install locally to project using `npm init -y`
* What Node.js is Used For
    * frameworks such as React and Angular rely on Node.js to create a sensible development environment where they can run
    * Node.js runs JS on server - single-thread server that's event-driven
        * everything that happens in Node.js is in reaction to an event
        * will register a callback before continuing to process the next event
        * uses libuv library to implement asynchronous behavior 
    * Execution model
        1) Node app passes async task to event loop along with a callback
        1) event loop efficiently manages a thread pool and executes tasks efficiently
        1) executes each callback as tasks complete
    * Downsides
        * single-thread imposes some limitations
        * need to use callback-based style of coding - promises improve flow control in modern JS
    * Server
        1) open browser and local host `http://localhost:3000`
        1) `http.createServer()` 
        1) anonymous function called with request and response arguments
        1) tell server to listen for incoming requests
    * Apps suited to Node.js
        * apps requiring some form of real-time interaction or collaboration
            * chat sites
            * live streams
            * API building
        * can use boilerplate eg: Express
    * Advantages of Node.js
        * speed
        * scalability
        * can do everything in same language
        * speaks JSON
            * data exchange format
            * interacts with object databases eg: MongoDB
    * Other Uses
        * scripting language to automate repetitive or error prone tasks 
        * write own command line tools
        * build cross-platform desktop apps
