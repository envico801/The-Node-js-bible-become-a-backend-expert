Q: What are magic strings?  
A: A magic string is a string that declares directly in several places in a code without assigning it to a variable.  
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


---

DECK INFO

TARGET DECK: Javascript::Node::MTNBB - The node js bible become a backend expert - marluan espiritusanto::Part VII - Synchrony vs Asynchrony::Chapter 4 - Event Emitter

FILE TAGS: Javascript Node

Tags:

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store