---
title:
Post: It's not Hip to be Square (in Java)
---

by Rachel Turek Sullivan

**Why is a square a bad example of object inheritance?**

In <a href="https://retsullivan.github.io/Your-Mother-was-a-Toaster-and-your-Father-Smelled-of-Class-Inheritance/" target="_blank">yesterday's post</a>, I compared class inheritance in Java to how quadrilaterals are related to each other. Tim pointed out that while it's a decent analogy when considering quadrilaterals, parallelograms, and rectangles, the mapping breaks down when you consider squares.

In Java, though classes can inherit properties from multiple parent classes, they can only access one set of properties at a time. Suppose that quadrilateral was a parent class in Java. A parallelogram inherits the property of “has 4 sides” from it’s parent, quadrilateral. Both rectangles and rhombuses are special types of parallelograms - for example they both have the property of “opposite sides parallel”. In this scenario they are could be called sibling classes with the same parent (parallelogram). 

The issue with squares is that, in mathematics, they have all the properties of both rectangles and rhombi. A square is a rhombus, and a square is a rectangle - it has all the features of both categories. If I have a square, I can assume that it has 4 equal angles (a property of rectangles) *and* 4 equal sides (a property of rhombi).  

This dual inheritance is not something that is allowed in Java classes.  A square is a bad example of inheritance because (in mathematics) it inherits from more than one direct parent.  Because of this, trying to create code in which squares inherit area or perimeter calculators (or even something as simple as setting the length and width) from a rectangle parent class violates best OOP coding practices (in particular the <a href="https://dzone.com/articles/the-liskov-substitution-principle-with-examples" target="_blank">Liskov Substitution principle</a>).

The Liskov Substitution Principle (LSP) states that all instances of a parent class should be replaceable with any instance of a child class without the user knowing the difference and without causing any issues in the program. Suppose, S and R are objects, and S subclass on R. If LSP is not carefully followed when creating the subclass S, there is could be an operation accessible through the interface of R which behaves differently when applied to S. So code written to work with the parent class R will not expect the outlier behavior and maybe not function as intended. 
