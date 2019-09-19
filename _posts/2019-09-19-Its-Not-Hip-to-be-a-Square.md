
---
title:
It's not Hip to be Square (in Java)
___

**Why is a square a bad example of object inheritance?**

In <a href="https://retsullivan.github.io/Your-Mother-was-a-Toaster-and-your-Father-Smelled-of-Class-Inheritance/" target="_blank">yesterday's post</a>, I compared class inheritance in Java to how quadrilaterals are related to each other. Tim pointed out that while it's a decent analogy when considering quadrilaterals, parallelograms, and rectangles, the mapping breaks down when you consider squares.

In Java, though classes can inherit properties from multiple parent classes, they can only access one set of properties at a time. Suppose that quadrilateral was a parent class in Java. A parallelogram inherits the property of “has 4 sides” from it’s parent, quadrilateral. Both rectangles and rhombuses are special types of parallelograms - for example they both have the property of “opposite sides parallel”. In this scenario they are could be called sibling classes with the same parent (parallelogram). 

The issue with squares is that, in mathematics, they have all the properties of both rectangles and rhombi. A square is a rhombus, and a square is a rectangle - it has all the features of both categories. If I have a square, I can assume that it has 4 equal angles (a property of rectangles) *and* 4 equal sides (a property of rectangles).  

This dual inheritance is not something that is allowed in Java classes.  A square is a bad example of inheritance because (in mathematics) it inherits from more than one direct parent.

A better mathematical corollary might be types of Real numbers. 

![](https://cdn1.byjus.com/wp-content/uploads/2019/04/Real-Numbers-Chart.png)


In this scenario, each type of number only inherits from a single parent class. A good way to visualize this is though grouping the numbers inside circles.


![](http://cyclesrecycled.com/wp-content/uploads/2018/05/classifying-real-numbers-worksheets-pdf-classification-of-diagram-are-made-up-five-different-types-as.jpg)

Consider the number 5, a natural number. The circle for natural numbers is enclosed by the circles for Whole, Integer, Rational and Real, making 5 fall within those circles as well. This is because 5 is a natural number, whole number, an integer, a rational number, and a real number. "5" has all the traits of an integer, because Natural numbers are a type of whole number, which is a type of integer.

Inside the real numbers are two types of numbers - rational and irrational.  Those types are mutually exclusive - no numbers exist that can belong to both the rationals and irrationals.  In this scenario, irrational and rational numbers inherit algebraic properties from their "parent" (the real numbers), but each have unique traits that are different from each other. A rational number **can** be written as a ratio of two integers.  An irrational number **cannot** be written as a ratio of two integers.  Thus, no number could be in both categories at the same time. 

If we think of the real numbers as a parent class, the rational and irrational numbers are sibling classes that share real numbers as a parent class. Integer, whole, and natural numbers are the descendants of rationals. This example, though not perfect, conforms more closely to class inheritance than that of the quadrilaterals. 
