---
layout: post
title: 16 Boolean Operators and Expressions and Where to Find Them
---
##Boolean Logic

Boolean logic is a simple but powerful concept that is the foundation of many mathematical and scientific fields.  It is fundamental to software programming, because it is able to help developers breakdown complex statements into easy to digest logical formulas. 

Boolean logic uses bools (true and false values) to organize information. Bools are typically denoted as T or 1 for true and F or 0 for false.  A Boolean operator in Java programming is an operator that returns a Boolean result that’s based on the Boolean result of one or two other expressions. Boolean variables can have two values - “true” or “false”.

##Using Boolean Logic on a Single Element

The negation operator is written as “!”. The term “!a” is read as “not a”. When applied to bools, we can create a truth table to list all the possible logical outcomes.

##Truth Table for Negation

a |!a
------------ | -------------
T|F
F|T

When considering a single variable boolean, we see that if a bool (a) is true than its opposite (!a) is false.  Likewise if a bool (a) is false, it’s opposite (!a) must be true. In Java, the ! operator returns true if the operand to the right evaluates to false.  It returns false if the operand to the right is true.

Using Boolean Logic on two elements

Two more important Boolean operators are “And” and “Or”.  In Java, the comparison operator “And” is written “&&”, and "Or" is written as  “||”.  Truth tables with two boolean elements are more complicated because we have to compare two bools to create our final true or false declaration.

##Truth Table for Or 
a|b|AorB
------------ | ------------- | -------------
T|T|T
F|T|T
T|F|T
F|F|F


##Truth Table for And "&&"
a|b|"A&&B"
------------ | ------------- | -------------
T|T|T
F|T|F
T|F|F
F|F|F

Included in the table below is a concept called “exclusive or”.  This is a logical concept that does not have a character exclusive operator in Java.  However, we can construct the logic behind it through a bit of code (seen in the table below) that combines the || and && operators. In simple language, exclusive or means “this or that, but not both".

##Truth Table for Exclusive Or
a | b | A XOR B
------------ | ------------- | -------------
T|T|F
F|T|T
T|F|T
F|F|F

Boolean operators are used in loops to determine if the program should enter a loop, or continue to pass through a loop.  The table below contains some pseudocode examples and brief explainations.

Operator | Code | Explaination
------------ | ------------- | -------------
!|if( !a){ //do code}|This will execute only if A is not true
or|if (a||b){	//do code}|This will execute as long as ONE of the elements is TRUE
&&|if (a&&b){//do code}|This will execute ONLY if BOTH a and b are TRUE
XOR|public static boolean logicalXOR(boolean x, boolean y) { return ( ( x || y ) && ! ( x && y ) ); }|There is no character exclusive or operator in java.  However, one can create the logic though combining the || and && operators. This will only execute if the truth values don’t match.



