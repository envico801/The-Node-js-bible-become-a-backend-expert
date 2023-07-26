Q: What is the event loop?  
A: We could say that **it is a connector between worlds**, on the one hand **the event queue** (that have environments like node or chrome, etc) **and** on the other hand **the callstack** (by the javascript engine V8), **it is used to handle asynchronous events because javascript is synchronous**, first priority is given to the actions that are in the callback and then once it is emptied will begin to run the events in the queue.
<!--ID: 1690389246827-->

---

DECK INFO

TARGET DECK: Javascript::Node::MTNBB - The node js bible become a backend expert - marluan espiritusanto::Part VII - Synchrony vs. Asynchrony::Chapter 5 - Libuv, Event Loop and Non-Blocking IO?

FILE TAGS: Javascript Node

Tags:

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store