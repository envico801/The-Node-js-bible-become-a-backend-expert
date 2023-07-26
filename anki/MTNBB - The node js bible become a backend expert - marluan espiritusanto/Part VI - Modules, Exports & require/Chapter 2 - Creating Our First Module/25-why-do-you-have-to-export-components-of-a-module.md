Q: Why do you have to export components of a module?  
A: Because everything that is not plain code will require you to export it explicitly, for example:
```javascript
function myFunction() {
  return 'Hi!';
}
module.export = myFunction;
// ---
const importedFun = require('./myModule');
importedFun(); // "Hi!"
```
<!--ID: 1690389246886-->

---

DECK INFO

TARGET DECK: Javascript::Node::MTNBB - The node js bible become a backend expert - marluan espiritusanto::Part VI - Modules, Exports & require::Chapter 2 - Creating Our First Module

FILE TAGS: Javascript Node

Tags:

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store