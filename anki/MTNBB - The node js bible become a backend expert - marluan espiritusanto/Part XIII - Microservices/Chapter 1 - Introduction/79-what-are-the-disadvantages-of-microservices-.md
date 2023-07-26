Q: What are the disadvantages of microservices?  
A: 1.Difficult to test (together) e.g. (if we have 1000 microservices we have to do an independent deployment of each one of them and also test them globally all together).  
2.Possibility of duplication e.g. (it can happen that there are so many microservices that microservices with the same functionality are created).  
3.Information integrity e.g. (ideally each microservice would have to have a totally different database, but then it may be the case that in one of these databases there is duplicity and not in another. In these cases it is necessary to know that the architecture must be respected so that the integrity of the information/data is maintained).  
4.Specialized teams e.g. (developers are expected to have DevOps experience, they have to deliver the application, localized, tested, etc).
<!--ID: 1690389246720-->

---

DECK INFO

TARGET DECK: Javascript::Node::MTNBB - The node js bible become a backend expert - marluan espiritusanto::Part XIII - Microservices::Chapter 1 - Introduction

FILE TAGS: Javascript Node

Tags:

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store