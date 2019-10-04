---
layout: post
title: Lambda Lambda Lambda-- Revenge of the Functional Interfaces
---

## **Using Java Functional Interfaces with Lambda Expressions**


### **Lambda Expressions - "Look, Ma - No Objects!"**

Java lambda expressions were Java's first forray into the land of functional programming. Unlike everything else we've learned so far about Java, lambda expressions are functions which can be created *without* being part of a class. Lambda expressions are a way to pass a function implementation as a parameter. 

When we use lambda expressions, we don't have to declare a type.  This is because we are using them to act on methods from Functional Interfaces that define the variable types for us. This is called *type inference*.  Another example of type inference in Java is using "var" when we're declaring a new vairable.

Lambda expressions have two parts:

    ( formal-parameter-list )  -> { expression-or-statements }

The class examples below use a functional interface called `IntMath`.  It defines the parameters for one method, `.doMath()`, as two integers.

    public interface IntMath {
       int doMath(int x, int y);
    }


Consider `.addition_with_lambda()` in the next block of code. It has one method `.doMath()` whose operation in the `.additionwithlambda()` method is defined by the lambda expression `a+b`.

    @Test
    void addition_with_lambda(){
    IntMath math = (a,b) -> a+b;
    assertEquals(5, math.doMath(2,3));
    }

Using lambda expressions here allowed us to define a simple addition function to use in the `addition_with_lambda` method without declaring a whole seperate class that implements the `IntMath` interface. 

### **Functional Interfaces**

Any interface with a SAM(Single Abstract Method) is a functional interface. SAMs are different from regular interfaces because they can only have one abstract method for which they define parameters. This is becuase SAMs were created to work with lamda expressions.

A little digging yielded this list of <a href="https://www.tutorialspoint.com/java8/java8_functional_interfaces.htm" target="_blank">43 functional interfaces</a> available in Java. Here are some definitions of a few of the functional interfaces that we've used or discussed in bootcamp:

Functional Interface examples:
* Function - receives one value and returns another
* Consumer - receives one value but doesn't return one
* Supplier - supplies results of a certain type (boolean, int, etc.)
* Comparator - compares two pieces of data
* Predicate - Represents a predicate (Boolean-valued function) of one argument.


And now for something <a href="https://www.youtube.com/watch?v=1mRG2oAQhso" target="_blank">completely different</a> as your reward for slogging through this whole post.