---
layout: post
title: Your Mother was a Toaster and your Father Smelled of Class Inheritance
---

By Rachel Turek Sullivan

## 

Today in improving BOOTCAMP, we were introduced to classes.  Classes are fundamental to Object Oriented Programming (OOP), so understanding how they work is essential to learning how to create easy to follow program structures.  One important characteristic of classes is the idea of inheritance.  

A class that inherits the properties of another class is known as child class (also derived class or sub class). A class whose properties other classes inherit is known as parent class (also called a base class or superclass ). 

## Inheritance in Mathematics

An easy way to think about inheritance is to revisit basic Geometry.  In high school geometry, students learn about many types of geometric shapes.  One important family of polygons is the quadrilaterals (shapes with 4 sides).  

![](https://www.onlinemathlearning.com/image-files/relationship-quadrilaterals.png)

The shapes at the bottom of the above chart have all the properties that the ones above them do, plus their own unique properties.  If I know that a shape is a square, I can assume that all angles are 90 degrees. I can also assume that it has 4 sides, and that opposite sides are parallel. This is because a square belongs to the rectangle family, which belongs to the parallelogram family, which belongs to the quadrilateral family.

In this analogy, the basic parent class is "Quadrilateral".  One of its child classes is "Parallelogram".  "Parallelogram" is an example of a class that is both inherits (from "Quadrilateral") and inherited from (by "rectangle" and "square").

## Cooking Classes

A more abstract thought exercise would be to examine the relationships between common kitchen objects, and how they could be types of classes. In class, Tim gave the example of a toaster being the child of the heating element class, which in turn is the child of electrical appliances.

For another example, consider the ever useful insulated travel mug.  It keeps my coffee safe and warm, and keeps me awake at Bootcamp. A travel mug is a special kind of coffee mug.  A mug is a type of cup. So if I know that I have a travel mug, I know that it can hold warm things like a mug, and hold liquids since a cup does.

In this scenario, the more general category, "cup" is the parent class. "Mug" is the child, which inherits its liquid holding abilities from "cup".  "Travel Mug" is able to hold hot liquids (thanks to inheriting from"mug" and "cup"), and has special insulating and spill prevention properties. 

## Cooking up Code

A little bit of pseudo-code gives us another sip of understanding of the Cup class and its descendants. 
```
public class Cup {
    Shape: Cylindrical;
    Ability: Holds liquid;
}

public class Mug extends Cup {
    Material: Ceramic;
    Ability: Can hold hot things;
}

public class TravelMug extends Mug {
    Protection: Lid;
    Ability: Insulating;
}
```

In this pseudocode, it may appear that Mug only has two traits (Ceramic and holding hot things).  However, because it *extends* the Cup class, we can also assume that it holds liquid and is cylindrical.  

Similarly, we know that if I have a favorite travel mug (`new TravelMug myFavoriteMug`), I can assume that it can do everything a cup or mug can do (since TravelMug inherits from mug, which inherits from cup. 
```
myFavoriteMug.isCylindrical();
myFavoriteMug.isCeramic();
myFavoriteMug.hasLid();
```        
These psuedo-methods would all return true, since `myFavoriteMug` is of class TravelMug.

## After Dinner Coffee

Good programmers keep their classes as lean and bite size as possible, so that their programs are well structured and easy to follow. I hope that envisioning classes as shapes and kitchen objects made these concepts easier to digest!












