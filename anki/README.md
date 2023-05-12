# MTNBB - The node.js bible become a backend expert - marluan espiritusanto

## Questions

### 3. V8 and JavaScript Engines

#### C1

Q: What is a processor (in a computer)?  
A: The processor is the brain of the system, it processes everything that happens on the PC and executes all the actions that exist.

Q: What is machine code (processor languages)?  
A: They are languages or code that the processor understands (low level) and that allow us to interact with it.

#### C2

Q: What is ECMA?  
A: It is an organization for information and communication systems.

Q: What is ECMAScript?  
A: It is the "rules" that govern the current javascript language. It was created because in the past browser manufacturers began to create their own interpretations of the language and with them came small adjustments and differences.

Q: In what year was the ES5 version of javascript released?  
A: 2009

Q: In which year was the ES6 version of javascript released?  
A: 2015

Q: What is ES Next?  
A: It is all the versions after ES6 (ES6 onwards).

Q: What is an engine (as far as javascript is concerned)?  
A: It is a program that converts javascript code into something that the processor can understand.

#### C3

Q: What is the V8 engine?  
A: It is the javascript engine used by google chrome and node.

### 4. JavaScript on the server: Node.js

#### C1

Q: What is a server (in its simplest form)?  
A: It is a computer that is providing services, it performs the work that is requested of it.

Q: What is the standard format of communication between a client and a server?  
A: HTTP

Q: What is AJAX?  
A: It is a technique used for asynchronous communication between a client and a server.

### 5. JavaScript (ES6+) Review

#### C2

Q: What is an expression?  
A: It is anything that produces a data type (Object, String, Number, Boolean, Array, Set, Map, Function, Symbol, undefined, null, etc...).

```javascript
const test = 34; // 34 is an expression
```

Q: What are the javascript collections?  
A: Array, Set, Map

#### C4

Q: What is a variable?  
A: It is a space in memory that is used to store data and to access this space a name is used, as if it were the key to a door.

#### C5

Q: What is a logical operator (what does it allow us to do)?  
A: It allows us to combine several expressions and from them produce a boolean value.

#### C6

Q: What is a conditional?  
A: It is a piece of code that allows us to evaluate if a condition is met and based on that to do something.

#### C11

Q: What is a callback?  
A: It is a function that is passed as an argument to another function to execute it. Usually the function that is passed as an argument is a pointer/address in memory.

Q: What is the first parameter in a callback function?  
A: The first parameter should correspond to an error (if any).

#### C16

Q: What happens when we add the word async to a function?  
A: This will cause the function to return a promise.

Q: What happens when the await word is called?  
A: Calling the await word causes the execution of a function to pause (in most cases) until a promise is resolved or rejected. It will return a completed promise

### 6. Modules, exports & require

#### C1

Q: What is a module?  
A: It is a reusable block of code whose existence does not accidentally affect other code.

Q: What is CommonJS?  
A: It is a set of rules for how code modules should be structured.

#### C2

Q: Why does node create a module cache?  
A: Because by requiring a module node will "cache" the content of the module using a singleton (a single instance) that will be stored in memory during the execution of the code.

Q: Why do you have to export components of a module?  
A: Because everything that is not plain code will require you to export it explicitly, for example:

```javascript
funcion asd() {
    return "asd"
}

module.export = asd
// ---
const asdFun = require("./myModule")
asdFun() // "asd"
```

Q: In what order node looks for the available modules?  
A: It looks for them first in the main directory and if it doesn't find them there it will look for them in "./node_modules", if it doesn't find them there it will produce an error.

### 7. Synchrony vs. Asynchrony

#### C1

Q: What is asynchrony?  
A: It is more than one process/thing running simultaneously.

Q: Does Node do things asynchronously?  
A: Yes, but its engine (v8) does them synchronously.

Q: What is synchrony?  
A: One process or one thing running at a time.

Q: Why is javascript said to be synchronous?  
A: Because it executes line by line, it was designed for that, there is always only 1 thing running at any given time.

#### C2

Q: What is an event?  
A: It is something that has happened in our application that we can respond to, this concept is found in many areas of software architecture.

Q: Why is it said that nodejs has 2 types of events?  
A: They are often connected to each other, but node on the one hand handles the system events (C++, the nodejs core) thanks to the livuv library.
On the other hand there are the custom events that are triggered by the event handler inside the javascript core. They are handled by another library that deals with events (where basically something happens and we can respond).

Q: What kind of events does livuv send?  
A: Sends events that are happening inside the computer system (low level).

Q: Why is it said that the 2 types of events that exist in node are connected?  
A: Because many times the events that are executed at system level (with the livuv library) are forwarded by the javascript event handler, that's why many times they are confused with only 1 thing

Q: Why is it said that there are no "real" events in javascript?  
A: Javascript does not have the concept of "event" (there is no event type), in reality what is happening is a "trick" (it is a simulation, it is just an object with properties).

Q: Why is the term "syntactic-sugar" used when talking about classes?  
A: Because it is used to simulate the behavior of first-order functions.

#### C4

Q: What are magic strings?  
A: A magic string is a string that declares directly in several places in a code without assigning it to a variable. According to magic strings, a program’s behavior can change. Examples of magic strings include cache keys, specific URL patterns, prefixes, user types.

```javascript
function myFun(foo) {
  if (foo == 'bar') {
    // do something
  }
}
// and someone accidentally types:
myFun('barr');
```

#### C5

Q: Is the event loop concept part of the javascript engine (V8) or of the livuv library?  
A: The event loop is part of the livuv library, it is something that is usually implemented by each javascript runtime environment to handle asynchronism, for example, the browser also implements its own version without using the livuv library.

Q: What is the event loop?  
A: We could say that it is a connector between worlds, on the one hand the event queue (that have environments like node or chrome, etc) and on the other hand the callstack (by the javascript engine V8), it is used to handle asynchronous events because javascript is synchronous, first priority is given to the actions that are in the callback and then once it is emptied will begin to run the events in the queue.

Q: What is non-blocking IO?  
A: It is the ability to do actions without pausing or stopping other actions (as long as it is done correctly).

---

TARGET DECK: Javascript::Node::MTNBB - The node.js bible become a backend expert - marluan espiritusanto

FILE TAGS: Javascript Node

Tags:

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```
