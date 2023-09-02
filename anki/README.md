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

Q:: What is a processor (speaking of computers)?  
A:: The processor is the brain of the system, it processes everything that happens on the PC and executes all the actions that exist.

Q:: What are processor languages (machine code)?  
A:: They are languages or codes that the processor understands (at a low level) and that allow us to interact with it.

#### Chapter 2 - ECMA, ECMAScript and JavaScript Engines

Q:: What is ECMA?  
A:: It is an organization for information and communication systems.

Q:: What is ECMAScript?  
A:: It is the "rules" that govern the current javascript language. It was created because in the past browser manufacturers began to create their own interpretations of the language and with them came small adjustments and differences.

Q:: In what year was the ES5 version of javascript released?  
A:: 2009

Q:: In which year was the ES6 version of javascript released?  
A:: 2015

Q:: What is ES Next?  
A:: It is all the versions after ES6 (ES6 onwards).

Q:: What is an engine (as far as javascript is concerned)?  
A:: It is a program that converts javascript code into something that the processor can understand.

#### Chapter 3 - V8

Q:: Where is the V8 javascript engine used?  
A:: It is the javascript engine used by google chrome and node.

#### Chapter 4 - Configuring Visual Studio Code

#### Chapter 5 - Adding Behavior to Node.js Core

### Part IV - JavaScript on the Server: Node.js

#### Chapter 1 - Client and Server

Q:: What is a server (in its simplest form)?  
A:: It is a computer that is providing services, it performs the work that is requested of it.

Q:: What is the standard format of communication between a client and a server?  
A:: HTTP (Hypertext Transfer Protocol)

Q:: What is AJAX?  
A:: It is a technique used for asynchronous communication between a client and a server.

#### Chapter 2 - JavaScript Code on the Server?

#### Chapter 3 - [BOOK]: Learn more about Node.js

### Part V - JavaScript Review (ES6+)

#### Chapter 1 - Introduction

#### Chapter 2 - Expressions?

Q:: What is an expression?  
A:: It is anything that produces a data type (Object, String, Number, Boolean, Array, Set, Map, Function, Symbol, undefined, null, etc...).

```javascript
const test = 34; // 34 is an expression
```

Q:: What are the javascript collections?  
A:: Array, Set, Map

#### Chapter 3 - Value Types in JavaScript

#### Chapter 4 - Variables

Q:: What is a variable?  
A:: It is a space in memory that is created to store data and a name is used to access this space. You can imagine it as the key to a door.

#### Chapter 5 - Logical operators

Q:: What is a logical operator (what does it allow us to do)?  
A:: It allows us to combine several expressions and from them produce a boolean value.

#### Chapter 6 - Conditionals

Q:: What is a conditional?  
A:: It is a piece of code that allows us to evaluate if a condition is met and based on that to do something.

#### Chapter 7 - Objects

#### Chapter 8 - Collections

#### Chapter 9 - Loops

#### Chapter 10 - Functions

#### Chapter 11 - Theory: Callbacks

Q:: What is a callback?  
A:: It is a function that is passed as an argument to another function to execute it. Usually the function that is passed as an argument is a pointer/address in memory.

Q:: What is the first parameter in a callback function?  
A:: The first parameter should correspond to an error (if any).

#### Chapter 12 - Practice: Callbacks

#### Chapter 13 - Callback hell

#### Chapter 14 - Theory: Promises

#### Chapter 15 - Practice: Promises

#### Chapter 16 - Theory: Async/Await

Q:: What happens when we add the word async to a function?  
A:: This will cause the function to return a promise. And it also allows us to use the "await" word to handle other promises within the function.

Q:: What happens when the await word is called?  
A:: Calling the await word causes code execution to pause until a promise is resolved or rejected. It will return a completed promise

#### Chapter 17 - Practice: Async/Await

#### Chapter 18 - Conclusion

#### Chapter 19 - Additional Resources for Further Reading in JavaScript

#### Chapter 20 - [BOOK]: Learn more about JavaScript

### Part VI - Modules, Exports & require

#### Chapter 1 - What the heck is a module?

Q:: What is a module?  
A:: It is a reusable block of code whose existence does not accidentally affect other code.

Q:: What is CommonJS?  
A:: It is a set of rules for how code modules should be structured. Its format has been heavily influenced by NodeJS module management.

#### Chapter 2 - Creating Our First Module

Q:: Why does node create a module cache?  
A:: Because by requiring a module node will "cache" the content of the module using a singleton (a single instance) that will be stored in memory during the execution of the code.

Q:: Why do you have to export components of a module?  
A:: Because everything that is not plain code will require you to export it explicitly, for example:

```javascript
function myFunction() {
  return "Hi!";
}
module.export = myFunction;
// ---
const importedFun = require("./myModule");
importedFun(); // "Hi!"
```

Q:: In what order node looks for the available modules?  
A:: It looks for them first in the main directory and if it doesn't find them there it will look for them in "./node_modules", if it doesn't find them there it will produce an error.

### Part VII - Synchrony vs. Asynchrony

#### Chapter 1 - Introduction

Q:: What is asynchrony?  
A:: It is more than one process/thing running simultaneously.

Q:: Does Node do things asynchronously?  
A:: Yes, but its engine (v8) does them synchronously.

Q:: What is synchrony?  
A:: One process or one thing running at a time.

Q:: Why is javascript said to be synchronous?  
A:: Because it executes line by line, it was designed for that, there is always only 1 thing running at any given time.

#### Chapter 2 - What really are Events?

Q:: What is an event?  
A:: It is a situation that has happened in our application, to which we can respond. This concept is found in many areas of software architecture.

Q:: Why is it said that nodejs has 2 types of events?  
A:: They are often connected to each other, but **node** on the one hand **handles the system events (C++, the nodejs core) thanks to the livuv library**.  
On the other hand there are the **custom events that are triggered by the event handler inside the javascript core**.

Q:: What kind of events does livuv send?  
A:: Livuv sends events that are occurring within the computer system (at a low level).

Q:: Why is it said that the 2 types of events that exist in node are connected?  
A:: Because many times the events that are executed at system level (with the livuv library) are forwarded to the javascript event handler, that's why many times they are confused with only 1 thing.

Q:: Why is it said that there are no "real" events in javascript?  
A:: Javascript does not have the concept of "event" (there is no event type), in reality what is happening is a "trick" (it is a simulation, it is just an object with properties).

Q:: Why is the term "syntactic-sugar" used when talking about classes?  
A:: Because it is used to simulate the behavior of first-order functions.

#### Chapter 3 - Creating Our Own Event Emitter

#### Chapter 4 - Event Emitter

Q:: What are magic strings?  
A:: A magic string is a string that declares directly in several places in a code without assigning it to a variable.  
According to magic strings, a program’s behavior can change.  
Examples of magic strings include cache keys, specific URL patterns, prefixes, user types.

```javascript
function myFun(foo) {
  if (foo == "bar") {
    // do something
  }
}
// and someone accidentally types:
myFun("barr");
```

#### Chapter 5 - Libuv, Event Loop and Non-Blocking IO?

Q:: Is the event loop concept part of the javascript engine (V8) or of the livuv library?  
A:: The event loop is part of the livuv library, it is something that is usually implemented by each javascript runtime environment to handle asynchronism, for example, the browser also implements its own version without using the livuv library.

Q:: What is the event loop?  
A:: We could say that **it is a connector between worlds**, on the one hand **the event queue** (that have environments like node or chrome, etc) **and** on the other hand **the callstack** (by the javascript engine V8), **it is used to handle asynchronous events because javascript is synchronous**, first priority is given to the actions that are in the callback and then once it is emptied will begin to run the events in the queue.

Q:: What is non-blocking IO?  
A:: It is the ability to do actions without pausing or stopping other actions (as long as it is done correctly).

### Part VIII - HTTP Protocol and Web Servers

#### Chapter 1 - Introduction

Q:: What is HTTP?  
A:: It is the system that allows the transfer of information between different services and the clients that use web pages (or any application that invokes the HTTP protocol).

Q:: What is a web server?  
A:: It is the software that is responsible for delivering the content of a website to the user.

#### Chapter 2 - Creating Our First Web Server

#### Chapter 3 - Understanding Our First Web Server

#### Chapter 4 - Understanding Routes

#### Chapter 5 - Getting to Know Express.js

#### Chapter 6 - Understanding Routes with Express.js

Q:: For what purpose is the GET (HTTP) verb used?  
A:: To read a resource

Q:: For what purpose is the POST (HTTP) verb used?  
A:: To create a new resource

Q:: For what purpose is the PUT (HTTP) verb used?  
A:: To replace an existing resource

Q:: For what purpose is the PATCH (HTTP) verb used?  
A:: To update a property of a resource (often used interchangeably with the PUT verb, but PUT is used when you want to update a resource completely).

Q:: For what purpose is the DELETE verb (HTTP) used?  
A:: To remove a resource

#### Chapter 7 - Demonstration of the project we will create

#### Chapter 8 - Quotes Project: Part I

#### Chapter 9 - Quotes Project: Part II

Q:: What is middleware?  
A:: It is a block of code that runs between the request made by the user until the request reaches the server, it is an intermediary.

Q:: What is the MVC pattern?  
A:: Software design pattern for programming that proposes to separate the code of the programs by their different responsibilities.

#### Chapter 10 - Quotes Project: Part III

### Part IX - Databases

#### Chapter 1 - Introduction

Q:: From what year did SQL (relational) databases start to be used?  
A:: They started to be used in the 80's and until today they are still the most popular option.

Q:: What is a relational database?  
A:: The principle of relational databases is based on the organization of information in small pieces, which are related to each other through the relationship of identifiers.  
This allows to make relationships with other tables (which is the representation of the entity in the database).

Q:: What is ACID?  
A:: It means **Atomicity**, **Consistency**, **Isolation** and **Durability**.

Q:: What properties do relational databases bring to systems?  
A:: They bring properties that allow them to be more robust and less vulnerable to failures.

Q:: What is a NO-SQL (non-relational) database?  
A:: As its name suggests, non-relational databases are those that, unlike relational databases, do not have an identifier that serves as a relationship between one set of data and another. They are very useful when we do not have an exact schema of what is going to be stored.

Q:: What is an ORM?  
A:: **Object Relational Mapping**, is a programming model that consists of the transformation of the tables of a database, in a series of entities (a model, class or a simple object) that simplify the basic tasks of access to the data for the programmer.

Q:: What is an ODM?  
A:: It is the same as an ORM but it is intended for non-relational databases (NO-SQL).

#### Chapter 2 - Relational Databases with Sequelize

#### Chapter 3 - Continuing the Sequelize exercise

#### Chapter 4 - Non-relational databases with Mongoose

Q:: What is a cron job?  
A:: It is an extremely useful tool which is used to implement any repetitive task automatically.

Q:: What is web scraping?  
A:: It is a technique used by software programs to extract information from websites.

#### Chapter 5 - Cronjob with Mongoose

#### Chapter 6 - [BOOK]: Learn more about Sequelize

#### Chapter 7 - [BOOK]: Learn more about Mongoose

### Part X - Frontend and Backend

#### Chapter 1 - Introduction

Q:: What is the frontend?  
A:: It is the visual part (client) that is used to interact with any software or process.

Q:: What is the backend?  
A:: It is the part of a software that manipulates the business logic and data persistence (server).

Q:: What is a framework?  
A:: It is a conceptual and technological structure of defined support, usually with artifacts or concrete software modules, which can serve as a basis for the organization and development of software.

#### Chapter 2 - Section Preparations

#### Chapter 3 - Starting the backend structure

#### Chapter 4 - Configuring the backend assets

#### Chapter 5 - Model + seeder creation

#### Chapter 6 - Creating middlewares and routes

#### Chapter 7 - Frontend structure

Q:: What is typescript?  
A:: It is an open source programming language developed by Microsoft, which has object-oriented programming tools, very favorable if you have large projects.

Q:: What is a superset?  
A:: It is a programming language written on top of another language.

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

Q:: What is an API?  
A:: It is a set of definitions and protocols used to develop and integrate application software.

Q:: What is an architectural pattern?  
A:: It is a general and reusable solution to a common problem in software architecture within a given context.

Q:: What is the recommended use of "N-tier" (multi-tier) architecture?  
A:: It is recommended to use this architecture in desktop applications in general and in API's.

Q:: What is the recommended use of "client and server" architecture?  
A:: It is recommended to use this architecture in low coupling applications. Example, mobile applications and API's

#### Chapter 2 - RESTful?

Q:: What is REST?  
A:: It is an acronym for **Representational State Transfer**, an architectural style based on a set of predefined principles that describe how resources are defined and addressed through a web service.

Q:: What is RESTful?  
A:: Web service that implements REST principles.

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

Q:: What is monolithic architecture?  
A:: It is a single logical executable, a single autonomous unit, an example is the MVC pattern, where everything we need is in the same place.

Q:: What is vertical scaling?  
A:: Vertical scaling refers to scaling by adding more power (e.g. CPU, RAM) to an existing machine (also described as "scaling up").

Q:: What is horizontal scaling?  
A:: Horizontal scaling means scaling by adding more machines to your pool of resources (also described as "scaling out"). We would have to set up a load balancer, make sure that if one of our services stops working the others will pick up the slack, etc.

Q:: What is the recommended approach when starting to build an application?  
A:: It is recommended to start with a monolith and then as the demand increases you convert it into microservices.

Q:: What are the advantages of monolithic applications?  
A:: 1.Simple to develop  
2.Simple to test  
3.Easy to work alone  
4.Simple to deploy

Q:: What are the disadvantages of monolithic applications?  
A:: 1.They are not flexible e.g. (if we start with a programming language we have to finish with that one because we will not be able to change it).  
2.Difficult to maintain e.g. (the demand can make the application unsustainable).  
3.Difficult to scale e.g. (if you want to scale horizontally you have to duplicate the whole application instead of just 1 single component)  
4.Unreliable potential e.g. (if something is damaged inside the application, the whole application will be damaged).

Q:: What is microservices architecture?  
A:: It is a collection of small, autonomous services with unique responsibilities.

Q:: Is any small service a microservice?  
A:: No, microservices have the following characteristics:  
1.Single responsibility.  
2.They are persistent e.g. (data cannot be breached, lost, etc.).  
3.They are resilient e.g. (if a microservice crashes, it must know how to get up and know where it left off).  
4.They have logs e.g. (we should know at all times in what state and what our microservice has done, even what it is doing at the moment).  
5.They have a well defined API e.g. (I have to know if I am going to communicate with it with REST, rabbid enqueue, message broker, etc).

Q:: What are the advantages of microservices?  
A:: 1.Super easy to scale e.g. (if we have a service that is being consumed more than the others we only have to scale that one and not the whole application).  
2.Combination of technologies e.g. (we can take advantage of the different benefits of several programming languages).  
3.Reliable potential e.g. (we know the state in which each of the microservices is and we know that if any of them fails it must be able to get up again).  
4.Transparent Deploys e.g. (we can count on a CI/CD that will help us to bring a service to production with a simple commit).

Q:: What are the disadvantages of microservices?  
A:: 1.Difficult to test (together) e.g. (if we have 1000 microservices we have to do an independent deployment of each one of them and also test them globally all together).  
2.Possibility of duplication e.g. (it can happen that there are so many microservices that microservices with the same functionality are created).  
3.Information integrity e.g. (ideally each microservice would have to have a totally different database, but then it may be the case that in one of these databases there is duplicity and not in another. In these cases it is necessary to know that the architecture must be respected so that the integrity of the information/data is maintained).  
4.Specialized teams e.g. (developers are expected to have DevOps experience, they have to deliver the application, localized, tested, etc).

Q:: What is Kubernetes?  
A:: It is a container orchestrator that takes care of the maintenance of our applications.

Q:: What is an API gateway?  
A:: It is an entity that is in charge of receiving the requests and then it is going to pass it to the microservice responsible for responding.

#### Chapter 2 - Implementing Microservices

#### Chapter 3 - Better Understanding Microservices

#### Chapter 4 - Migrating from Monolithic to Microservices

#### Chapter 5 - More on Microservices Architecture

### Part XIV - CI/CD

#### Chapter 1 - Introduction

Q:: What is continuous integration?  
A:: It is a process where every change we make to our code must be tested and verified by the tests we have written beforehand.

Q:: What is continuous delivery?  
A:: It is similar to continuous integration, only in a more automated way and also our acceptance tests must be of high quality, because Continuous Delivery makes sure that every change we make is ready to be released to production.

Q:: What is continuous deployment?  
A:: As the name implies, we take care of continuous and automated deployments.

Q:: What is a pipeline?  
A:: It is a sequence of steps to be followed in a DevOps process.

#### Chapter 2 - CI/CD from our API

#### Chapter 3 - Some CI/CD and TravisCI Resources

### Part XV - Course Conclusion

#### Chapter 1 - Conclusion and Additional Recommendations

### Part XVI - Bonus

#### Chapter 1 - EXTRA CLASS

---

DECK INFO

TARGET DECK: Javascript::Node::MTNBB - The node js bible become a backend expert - marluan espiritusanto

FILE TAGS: #Javascript #Node

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```