---
{"dg-publish":true,"permalink":"/10-wiki/12-notes/chain-of-responsibility-20230228090935/"}
---

# Chain of Responsibility
---
[[10 Wiki/14 References/Books/Design Patterns - 0201633612\|Design Pattern]] for passing requests along a chain of handlers. Each handler decides whether to pass the request to the next or to stop it.

We create a Handler class describing a common interface, containing a single method to handle requests, and one more to set the next handler.

The concrete Handlers contain the code to handle the requests. They either modify and forward the request, or stop it.


###### META
Status:: #wiki/notes/mature 
Plantations:: [[10 Wiki/14 References/Books/Design Patterns - 0201633612\|Design Patterns]]
References:: [[10 Wiki/14 References/Books/Dive Into Design Patterns - 20230122071907\|Dive Into Design Patterns]]
