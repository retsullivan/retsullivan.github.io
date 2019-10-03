---
layout:post
title:GRASPing the Big Idea
---

## **General Responsibility Assignment Software Principals (GRASP)** 

GRASP are a collection of principles and patterns that work together to create best practices for software design.

![](https://raw.githubusercontent.com/retsullivan/retsullivan.github.io/master/images/GRASP.gif)

Alex covered 9 GRASP concepts this afternoon.  Here are the highlights:

## **Creators**

Today we discussed 3 types of creators. 

**Factory** 
* Provides an interface for creating objects in a superclass, but allows subclasses to alter the type of objects that will be created.
* Alex said it was sort of like BuildWorld (imagine if buildWorld could make different worlds...)

**Builder**
* Lets you construct complex objects step by step. 
* The pattern allows you to produce different types and representations of an object using the same construction code.
* Alex gave us a pizza factory code example in class

**Object Mother**
* An object mother is a special class used in testing
* Creates objects you can use for testing.
* Like a factory, but it’s for tests


## **Information Expert**
* Each object should have a single task or property on which they are the “Expert”.
* The goal of the Single Responsibility Principle is a program filled with information experts.


## **Low Coupling**

* Strives to reduce dependencies between parts of the codebase.
* Lowers the impact of change in one class.
* Makes code more reusable, maintainable and stable.
* Code may end up with many layers of indirection, which can make it hard for someone who didn’t write it to sort out.


## **High Cohesion**

* All your classes work well together.
* Keeps classes and objects well organized and understandable and supports low coupling.
* Our commands are a good example of high cohesion and fairly low coupling


## **Controller**

* Delegates how information is passed from one point to another in a program.
* ConsoleInputOutput is sort of an example in TAG.


## **Indirection**

* The process of breaking up chunks of work and having dedicated objects to work on each piece.
* TAG is a bad example - there are many places where we should have used indirection and split code off into other classes (obtaining an item from an adversary or treasure chest is a good example of where we could have used this concept)


## **Polymorphism**

* We’ve been using polymorphism when we override methods from a super class or interface. 
* Without using polymorphism, we have to depend on code tests to determine type of the object. As the system gets more complicated, we have to test for more types. This causes more coupling and less cohesion, which is the opposite of what we want.  
* BaseAliasedCommand and its children are good examples of using Polymorphism in TAG.  
* For more of my thoughts on polymorphisms, read about <a href="https://retsullivan.github.io/Tim's-Happy-Accident-a-Primer-on-Equality-in-Polymorphisms-on-Parent-and-Child-Classes/" target="_blank">Tim’s Happy Accident</a>


## **Protected Variations**

* Immutability
* Use objects and data encapsulation to protect important elements from variations on other elements.
* Uses interfaces, polymorphism, and methods like getters to access the information without changing it.


## **Pure Fabrication**

* Created when you, in the spirit of keeping your clases “Information Experts”, extract a task or functionality that was not part of the original purpose of the class. 
* If you find your code is essentially doing two things instead of one in an object, you should try and give it it’s own separate class to represent that functionality
* Example - making a “extract item” class to handle getting and setting items in from treasure chests and adversaries. Since my code uses the same process for each, this would be a good place to do this.
