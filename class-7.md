# Articles

## *What Google Learned From Its Quest to Build the Perfect Team*

* people working in teams have higher productivity
* right norms can raise group collective intelligence
* teams that did well on one assignment, did well on all
* functional groups:
    * speak roughly the same amount
    * social sensitivity/empathy
    * safe space
    * emotional conversations
    * listen to each other


## *Conversation about REST with my Brother*

* first part tells the browser what protocol to use
* stuff you type in there is one of the most important breakthroughs in the history of computing
    * it is capable of describing the location of something anywhere in the world from anywhere in the world
* whole world wide web is built on an architectural style called “REST”
    * REST provides a definition of a “resource”, which is what those things point to
* Those URLs tell the browser that there's a concept somewhere
    * can then go ask for a specific representation of the concept
    * the browser asks for the web page representation of the concept
* a resource has only a single representation
    * future = APIs
    * computers can use those same protocols to send messages back and forth to each other
* we need some way of having one machine tell another machine about a resource that might be on yet another machine
    * URL tells other machines where things are
    * Every programming language, database, or other kind of system has a different way of talking about nouns -- need URLs
    * polymorphism - different nouns can have the same verb applied to them
    * HTTP - applies nouns to verbs
* web pages are designed to be understood by people
    * retrieve  - HTTP GET
    * add something to another system - HTTP POST
    * replace - HTTP PUT
    * partial update - HTTP PATCH


## *SuperAgent*

*  light-weight progressive ajax API crafted for flexibility, readability, and a low learning curve
* request can be initiated by invoking the appropriate method on the request object, then calling .then() (or .end() or await) to send the request
