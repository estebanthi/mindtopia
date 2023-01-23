---
{"dg-publish":true,"permalink":"/10-wiki/12-notes/abstract-factory-20230122113146/"}
---

# Abstract Factory
---
This is a pattern that allows you to create families of related objects without specifying the concrete classes.

First, interfaces must be declared for each distinct product. We can make variants of products according to these interfaces.

We then declare an abstract factory, which is a class with methods for creating each product (e.g. createChair, createSofa...) returning the type represented by the interfaces written previously.

For each product variant, a factory is created according to the interface defined before. A factory only creates products of the same family, for example ModernChair, ModernSofa...


## Applications
- This pattern is used when you work with families of relative products, but you don't want the code to depend on the concrete classes of these products.

## Issues
- An application typically needs only one instance of a ConcreteFactory per product family. So it's usually best implemented as a [[100 Zettelkasten/Singleton\|Singleton]].
- AbstractFactory only declares an interface for creating products. It's up to ConcreteProduct subclasses to actually create them. The most common way to do this is to define a [[100 Zettelkasten/Factory Method\|Factory Method]] for each product.



###### META
Status:: #wiki/notes/mature 
Plantations:: [[100 Zettelkasten/Creational Patterns\|Creational Patterns]]
References:: [[10 Wiki/14 References/Goodreads/Dive Into Design Patterns - 20230122071907\|Dive Into Design Patterns]]
