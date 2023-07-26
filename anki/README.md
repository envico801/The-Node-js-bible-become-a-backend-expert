# MTNBB - The node js bible become a backend expert - marluan espiritusanto

## Questions

### Part I - Facilities and Preparations

#### Chapter 1 - Course Introduction

#### Chapter 2 - Course Scope

#### Chapter 3 - Course Topics

#### Chapter 4 - Course Requirements

#### Chapter 5 - Questions and Answers...

### Part II - Introduction and Scope

#### Chapter 1 - Facilities required to get started

#### Chapter 2 - Testing the Installations

### Part III - V8 and JavaScript Engines

#### Chapter 1 - Processors and Machine Code

P: What is a processor (speaking of computers)?  
R: The processor is the brain of the system, it processes everything that happens on the PC and executes all the actions that exist.

P: What are processor languages (machine code)?  
R: They are languages or codes that the processor understands (at a low level) and that allow us to interact with it.

#### Chapter 2 - ECMA, ECMAScript and JavaScript Engines

P: What is ECMA?  
R: It is an organization for information and communication systems.

P: What is ECMAScript?  
R: It is the "rules" that govern the current javascript language. It was created because in the past browser manufacturers began to create their own interpretations of the language and with them came small adjustments and differences.

P: In what year was the ES5 version of javascript released?  
R: 2009

P: In which year was the ES6 version of javascript released?  
R: 2015

P: What is ES Next?  
R: It is all the versions after ES6 (ES6 onwards).

P: What is an engine (as far as javascript is concerned)?  
R: It is a program that converts javascript code into something that the processor can understand.

#### Chapter 3 - V8

P: Where is the V8 javascript engine used?  
R: It is the javascript engine used by google chrome and node.

#### Chapter 4 - Configuring Visual Studio Code

#### Chapter 5 - Adding Behavior to Node.js Core

### Part IV - JavaScript on the Server: Node.js

#### Chapter 1 - Client and Server

P: What is a server (in its simplest form)?  
R: It is a computer that is providing services, it performs the work that is requested of it.

P: What is the standard format of communication between a client and a server?  
R: HTTP (Hypertext Transfer Protocol)

P: What is AJAX?  
R: It is a technique used for asynchronous communication between a client and a server.

#### Chapter 2 - JavaScript Code on the Server?

#### Chapter 3 - [BOOK]: Learn more about Node.js

### Part V - JavaScript Review (ES6+)

#### Chapter 1 - Introduction

#### Chapter 2 - Expressions?

P: What is an expression?  
R: It is anything that produces a data type (Object, String, Number, Boolean, Array, Set, Map, Function, Symbol, undefined, null, etc...).

```javascript
const test = 34; // 34 is an expression
```

P: What are the javascript collections?  
R: Array, Set, Map

#### Chapter 3 - Value Types in JavaScript

#### Chapter 4 - Variables

P: What is a variable?  
R: It is a space in memory that is created to store data and a name is used to access this space. You can imagine it as the key to a door.

#### Chapter 5 - Logical operators

P: What is a logical operator (what does it allow us to do)?  
R: It allows us to combine several expressions and from them produce a boolean value.

#### Chapter 6 - Conditionals

P: What is a conditional?  
R: It is a piece of code that allows us to evaluate if a condition is met and based on that to do something.

#### Chapter 7 - Objects

#### Chapter 8 - Collections

#### Chapter 9 - Loops

#### Chapter 10 - Functions

#### Chapter 11 - Theory: Callbacks

P: What is a callback?  
R: It is a function that is passed as an argument to another function to execute it. Usually the function that is passed as an argument is a pointer/address in memory.

P: What is the first parameter in a callback function?  
R: The first parameter should correspond to an error (if any).

#### Chapter 12 - Practice: Callbacks

#### Chapter 13 - Callback hell

#### Chapter 14 - Theory: Promises

#### Chapter 15 - Practice: Promises

#### Chapter 16 - Theory: Async/Await

P: What happens when we add the word async to a function?  
R: This will cause the function to return a promise. And it also allows us to use the "await" word to handle other promises within the function.

P: What happens when the await word is called?  
R: Calling the await word causes code execution to pause until a promise is resolved or rejected. It will return a completed promise

#### Chapter 17 - Practice: Async/Await

#### Chapter 18 - Conclusion

#### Chapter 19 - Additional Resources for Further Reading in JavaScript

#### Chapter 20 - [BOOK]: Learn more about JavaScript

### Part VI - Modules, Exports & require

#### Chapter 1 - What the heck is a module?

P: What is a module?  
R: It is a reusable block of code whose existence does not accidentally affect other code.

P: What is CommonJS?  
R: It is a set of rules for how code modules should be structured. Its format has been heavily influenced by NodeJS module management.

#### Chapter 2 - Creating Our First Module

P: Why does node create a module cache?  
R: Because by requiring a module node will "cache" the content of the module using a singleton (a single instance) that will be stored in memory during the execution of the code.

P: Why do you have to export components of a module?  
R: Because everything that is not plain code will require you to export it explicitly, for example:

```javascript
function myFunction() {
  return 'Hi!';
}
module.export = myFunction;
// ---
const importedFun = require('./myModule');
importedFun(); // "Hi!"
```

P: In what order node looks for the available modules?  
R: It looks for them first in the main directory and if it doesn't find them there it will look for them in "./node_modules", if it doesn't find them there it will produce an error.

### Part VII - Synchrony vs. Asynchrony

#### Chapter 1 - Introduction

P: What is asynchrony?  
R: It is more than one process/thing running simultaneously.

P: Does Node do things asynchronously?  
R: Yes, but its engine (v8) does them synchronously.

P: What is synchrony?  
R: One process or one thing running at a time.

P: Why is javascript said to be synchronous?  
R: Because it executes line by line, it was designed for that, there is always only 1 thing running at any given time.

#### Chapter 2 - What really are Events?

P: What is an event?  
R: It is a situation that has happened in our application, to which we can respond. This concept is found in many areas of software architecture.

P: Why is it said that nodejs has 2 types of events?  
R: They are often connected to each other, but **node** on the one hand **handles the system events (C++, the nodejs core) thanks to the livuv library**.  
On the other hand there are the **custom events that are triggered by the event handler inside the javascript core**.

P: What kind of events does livuv send?  
R: Livuv sends events that are occurring within the computer system (at a low level).

P: Why is it said that the 2 types of events that exist in node are connected?  
R: Because many times the events that are executed at system level (with the livuv library) are forwarded to the javascript event handler, that's why many times they are confused with only 1 thing.

P: Why is it said that there are no "real" events in javascript?  
R: Javascript does not have the concept of "event" (there is no event type), in reality what is happening is a "trick" (it is a simulation, it is just an object with properties).

P: Why is the term "syntactic-sugar" used when talking about classes?  
R: Because it is used to simulate the behavior of first-order functions.

#### Chapter 3 - Creating Our Own Event Emitter

#### Chapter 4 - Event Emitter

P: What are magic strings?  
R: A magic string is a string that declares directly in several places in a code without assigning it to a variable.  
According to magic strings, a program’s behavior can change.  
Examples of magic strings include cache keys, specific URL patterns, prefixes, user types.

```javascript
function myFun(foo) {
  if (foo == 'bar') {
    // do something
  }
}
// and someone accidentally types:
myFun('barr');
```

#### Chapter 5 - Libuv, Event Loop and Non-Blocking IO?

P: Is the event loop concept part of the javascript engine (V8) or of the livuv library?  
R: The event loop is part of the livuv library, it is something that is usually implemented by each javascript runtime environment to handle asynchronism, for example, the browser also implements its own version without using the livuv library.

P: What is the event loop?  
R: We could say that **it is a connector between worlds**, on the one hand **the event queue** (that have environments like node or chrome, etc) **and** on the other hand **the callstack** (by the javascript engine V8), **it is used to handle asynchronous events because javascript is synchronous**, first priority is given to the actions that are in the callback and then once it is emptied will begin to run the events in the queue.

P: What is non-blocking IO?  
R: It is the ability to do actions without pausing or stopping other actions (as long as it is done correctly).

### Part VIII - HTTP Protocol and Web Servers

#### Chapter 1 - Introduction

P: What is HTTP?  
R: It is the system that allows the transfer of information between different services and the clients that use web pages (or any application that invokes the HTTP protocol).

P: What is a web server?  
R: It is the software that is responsible for delivering the content of a website to the user.

#### Chapter 2 - Creating Our First Web Server

#### Chapter 3 - Understanding Our First Web Server

#### Chapter 4 - Understanding Routes

#### Chapter 5 - Getting to Know Express.js

#### Chapter 6 - Understanding Routes with Express.js

P: For what purpose is the GET (HTTP) verb used?  
R: To read a resource

P: For what purpose is the POST (HTTP) verb used?  
R: To create a new resource

P: For what purpose is the PUT (HTTP) verb used?  
R: To replace an existing resource

P: For what purpose is the PATCH (HTTP) verb used?  
R: To update a property of a resource (often used interchangeably with the PUT verb, but PUT is used when you want to update a resource completely).

P: For what purpose is the DELETE verb (HTTP) used?  
R: To remove a resource

#### Chapter 7 - Demonstration of the project we will create

#### Chapter 8 - Quotes Project: Part I

#### Chapter 9 - Quotes Project: Part II

P: What is middleware?  
R: It is a block of code that runs between the request made by the user until the request reaches the server, it is an intermediary.

P: What is the MVC pattern?  
R: Software design pattern for programming that proposes to separate the code of the programs by their different responsibilities.

#### Chapter 10 - Quotes Project: Part III

### Part IX - Databases

#### Chapter 1 - Introduction

P: From what year did SQL (relational) databases start to be used?  
R: They started to be used in the 80's and until today they are still the most popular option.

P: What is a relational database?  
R: The principle of relational databases is based on the organization of information in small pieces, which are related to each other through the relationship of identifiers.
This allows to make relationships with other tables (which is the representation of the entity in the database).

P: What is ACID?  
R: It means **Atomicity**, **Consistency**, **Isolation** and **Durability**.

P: What properties do relational databases bring to systems?  
R: They bring properties that allow them to be more robust and less vulnerable to failures.

P: What is a NO-SQL (non-relational) database?  
R: As its name suggests, non-relational databases are those that, unlike relational databases, do not have an identifier that serves as a relationship between one set of data and another. They are very useful when we do not have an exact schema of what is going to be stored.

P: What is an ORM?  
R: **Object Relational Mapping**, is a programming model that consists of the transformation of the tables of a database, in a series of entities (a model, class or a simple object) that simplify the basic tasks of access to the data for the programmer.

P: What is an ODM?  
R: It is the same as an ORM but it is intended for non-relational databases (NO-SQL).

#### Chapter 2 - Relational Databases with Sequelize

#### Chapter 3 - Continuing the Sequelize exercise

#### Chapter 4 - Non-relational databases with Mongoose

P: What is a cron job?  
R: It is an extremely useful tool which is used to implement any repetitive task automatically.

P: What is web scraping?  
R: It is a technique used by software programs to extract information from websites.

#### Chapter 5 - Cronjob with Mongoose

#### Chapter 6 - [BOOK]: Learn more about Sequelize

#### Chapter 7 - [BOOK]: Learn more about Mongoose

### Part X - Frontend and Backend

#### Chapter 1 - Introduction

P: What is the frontend?  
R: It is the visual part (client) that is used to interact with any software or process.

P: What is the backend?  
R: It is the part of a software that manipulates the business logic and data persistence (server).

P: What is a framework?  
R: It is a conceptual and technological structure of defined support, usually with artifacts or concrete software modules, which can serve as a basis for the organization and development of software.

#### Chapter 2 - Section Preparations

#### Chapter 3 - Starting the backend structure

#### Chapter 4 - Configuring the backend assets

#### Chapter 5 - Model + seeder creation

#### Chapter 6 - Creating middlewares and routes

#### Chapter 7 - Frontend structure

P: What is typescript?  
It is an open source programming language developed by Microsoft, which has object-oriented programming tools, very favorable if you have large projects.

P: What is a superset?  
R: It is a programming language written on top of another language.

#### Chapter 8 - TypeScript: Introduction

#### Chapter 9 - TypeScript: Types

#### Chapter 10 - TypeScript: Functions

#### Chapter 11 - TypeScript: Interfaces

#### Chapter 12 - TypeScript: Classes

#### Chapter 13 - TypeScript: Decorators

#### Chapter 14 - Getting to Know the Structure of an Angular 8+ Project

#### Chapter 15 - Getting Started with Angular 8+

#### Chapter 16 - Navbar Configuration

#### Chapter 17 - Configuring the HTTP Service

#### Chapter 18 - Connecting our frontend with the backend

#### Chapter 19 - Searching for technologies by their id

#### Chapter 20 - Implementing the search engine

#### Chapter 21 - Summary and final section code

#### Chapter 22 - [BOOK]: Learn more about TypeScript

### Part XI - Architecture for APIs

#### Chapter 1 - Introduction

P: What is an API?  
R: It is a set of definitions and protocols used to develop and integrate application software.

P: What is an architectural pattern?  
R: It is a general and reusable solution to a common problem in software architecture within a given context.

P: What is the recommended use of "N-tier" (multi-tier) architecture?  
R: It is recommended to use this architecture in desktop applications in general and in API's.

P: What is the recommended use of "client and server" architecture?  
R: It is recommended to use this architecture in low coupling applications. Example, mobile applications and API's

#### Chapter 2 - RESTful?

P: What is REST?  
R: It is an acronym for **Representational State Transfer**, an architectural style based on a set of predefined principles that describe how resources are defined and addressed through a web service.

P: What is RESTful?  
R: Web service that implements REST principles.

#### Chapter 3 - Getting Started

#### Chapter 4 - Project Presentation

#### Chapter 5 - Experimenting with the Architecture

#### Chapter 6 - Creating the models

#### Chapter 7 - Creating repositories

#### Chapter 8 - Creating services

#### Chapter 9 - Creating controllers

#### Chapter 10 - Creating routes

#### Chapter 11 - Authentication

#### Chapter 12 - Pagination

#### Chapter 13 - Caching

#### Chapter 14 - Implementing unit testing

#### Chapter 15 - Implementing Swagger

#### Chapter 16 - Troubleshooting and Finishing Touches

### Part XII - Docker

#### Chapter 1 - Introduction

#### Chapter 2 - How does Docker work?

#### Chapter 3 - Getting Started with Docker

#### Chapter 4 - Using Volumes

#### Chapter 5 - Dockerizing our API

#### Chapter 6 - More formal introduction to Docker

#### Chapter 7 - Docker from another point of view

#### Chapter 8 - Introduction to Docker by OpenCanarias

#### Chapter 9 - [BOOK]: Learn more about Docker

### Part XIII - Microservices

#### Chapter 1 - Introduction

P: What is monolithic architecture?  
R: It is a single logical executable, a single autonomous unit, an example is the MVC pattern, where everything we need is in the same place.

P: What is vertical scaling?  
R: Vertical scaling refers to scaling by adding more power (e.g. CPU, RAM) to an existing machine (also described as "scaling up").

P: What is horizontal scaling?  
R: Horizontal scaling means scaling by adding more machines to your pool of resources (also described as "scaling out"). We would have to set up a load balancer, make sure that if one of our services stops working the others will pick up the slack, etc.

P: What is the recommended approach when starting to build an application?  
R: It is recommended to start with a monolith and then as the demand increases you convert it into microservices.

P: What are the advantages of monolithic applications?  
R: 1.Simple to develop  
2.Simple to test  
3.Easy to work alone  
4.Simple to deploy

P: What are the disadvantages of monolithic applications?  
R: 1.They are not flexible e.g. (if we start with a programming language we have to finish with that one because we will not be able to change it).  
2.Difficult to maintain e.g. (the demand can make the application unsustainable).  
3.Difficult to scale e.g. (if you want to scale horizontally you have to duplicate the whole application instead of just 1 single component)  
4.Unreliable potential e.g. (if something is damaged inside the application, the whole application will be damaged).

P: What is microservices architecture?  
R: It is a collection of small, autonomous services with unique responsibilities.

P: Is any small service a microservice?  
R: No, microservices have the following characteristics:  
1.Single responsibility.  
2.They are persistent e.g. (data cannot be breached, lost, etc.).  
3.They are resilient e.g. (if a microservice crashes, it must know how to get up and know where it left off).  
4.They have logs e.g. (we should know at all times in what state and what our microservice has done, even what it is doing at the moment).  
5.They have a well defined API e.g. (I have to know if I am going to communicate with it with REST, rabbid enqueue, message broker, etc).

P: What are the advantages of microservices?  
R: 1.Super easy to scale e.g. (if we have a service that is being consumed more than the others we only have to scale that one and not the whole application).  
2.Combination of technologies e.g. (we can take advantage of the different benefits of several programming languages).  
3.Reliable potential e.g. (we know the state in which each of the microservices is and we know that if any of them fails it must be able to get up again).  
4.Transparent Deploys e.g. (we can count on a CI/CD that will help us to bring a service to production with a simple commit).

P: What are the disadvantages of microservices?  
R: 1.Difficult to test (together) e.g. (if we have 1000 microservices we have to do an independent deployment of each one of them and also test them globally all together).  
2.Possibility of duplication e.g. (it can happen that there are so many microservices that microservices with the same functionality are created).  
3.Information integrity e.g. (ideally each microservice would have to have a totally different database, but then it may be the case that in one of these databases there is duplicity and not in another. In these cases it is necessary to know that the architecture must be respected so that the integrity of the information/data is maintained).  
4.Specialized teams e.g. (developers are expected to have DevOps experience, they have to deliver the application, localized, tested, etc).

P: What is Kubernetes?  
R: It is a container orchestrator that takes care of the maintenance of our applications.

P: What is an API gateway?  
R: It is an entity that is in charge of receiving the requests and then it is going to pass it to the microservice responsible for responding.

#### Chapter 2 - Implementing Microservices

#### Chapter 3 - Better Understanding Microservices

#### Chapter 4 - Migrating from Monolithic to Microservices

#### Chapter 5 - More on Microservices Architecture

### Part XIV - CI/CD

#### Chapter 1 - Introduction

P: What is continuous integration?  
R: It is a process where every change we make to our code must be tested and verified by the tests we have written beforehand.

P: What is continuous delivery?  
R: It is similar to continuous integration, only in a more automated way and also our acceptance tests must be of high quality, because Continuous Delivery makes sure that every change we make is ready to be released to production.

P: What is continuous deployment?  
R: As the name implies, we take care of continuous and automated deployments.

P: What is a pipeline?  
R: It is a sequence of steps to be followed in a DevOps process.

#### Chapter 2 - CI/CD from our API

#### Chapter 3 - Some CI/CD and TravisCI Resources

### Part XV - Course Conclusion

#### Chapter 1 - Conclusion and Additional Recommendations

### Part XVI - Bonus

#### Chapter 1 - EXTRA CLASS

---

DECK INFO

TARGET DECK: Javascript::Node::MTNBB - The node js bible become a backend expert - marluan espiritusanto

FILE TAGS: Javascript Node

Tags:

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```
