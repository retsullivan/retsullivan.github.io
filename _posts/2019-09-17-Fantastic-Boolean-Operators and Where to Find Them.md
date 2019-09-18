---
layout: post
title: Fantastic Boolean Operators and Where to Find Them
---
<style>
.tablelines table, .tablelines td, .tablelines th {
        border: 1px solid black;
        }
</style>

By Rachel "Scamander" Sullivan

## Boolean Logic

Boolean logic is a simple but powerful concept that is the foundation of many mathematical and scientific fields.  It is fundamental to software programming, because it is able to help developers breakdown complex statements into easy to digest logical formulas. 

Boolean logic uses bools (true and false values) to organize information. Bools are typically denoted as T or 1 for true and F or 0 for false.  A Boolean operator in Java programming is an operator that returns a Boolean result that’s based on the Boolean result of one or two other expressions. Boolean variables can have two values - “true” or “false”.

## Using Boolean Logic on a single element

The negation operator is written as “~” for primitives and “!” for variables. The term “~a” is read as “not a”. When applied to bools, we can create a truth table to list all the possible logical outcomes.

## Truth Table for Negation

| A | !A |
|---|----|
| T | F  |
| F | T  |

When considering a single variable boolean, we see that if a bool (a) is true than its opposite (!a) is false.  Likewise if a bool (a) is false, it’s opposite (!a) must be true. In Java, the ! operator returns true if the operand to the right evaluates to false.  It returns false if the operand to the right is true.

## Using Boolean Logic on two elements

Two more important Boolean operators are “And” and “Or”.  In Java, the comparison operator “And” is written “&&”, and "Or" is written as  two vertical lines.  Truth tables with two boolean elements are more complicated because we have to compare two bools to create our final true or false declaration.

## Truth Table for Or 

|    A  	| B     	| A or B      	|
|-------	|-------	|-------------	|
| TRUE  	| TRUE  	| TRUE        	|
| FALSE 	| TRUE  	| TRUE        	|
| TRUE  	| FALSE 	| TRUE        	|
| FALSE 	| FALSE 	| FALSE       	|


## Truth Table for And "&&"

|          A 	| B     	| A &&  B (and) 	|
|------------	|-------	|---------------	|
| TRUE       	| TRUE  	| TRUE          	|
| FALSE      	| TRUE  	| FALSE         	|
| TRUE       	| FALSE 	| FALSE         	|
| FALSE      	| FALSE 	| FALSE         	|

Included in the table below is a concept called “exclusive or”.  This is a logical concept that does not have a character exclusive operator in Java.  However, we can construct the logic behind it through a bit of code (seen in the table below) that combines the || and && operators. In simple language, exclusive or mean “this or that, but not both’.

## Truth Table for Exclusive Or

|          A   	| B     	| A XOR B  	|
|--------------	|-------	|----------	|
| TRUE         	| TRUE  	| False    	|
| FALSE        	| TRUE  	| TRUE     	|
| TRUE         	| FALSE 	| TRUE     	|
| FALSE        	| FALSE 	| FALSE    	|

Boolean operators are used in loops to determine if the program should enter a loop, or continue to pass through a loop.  The table below contains some pseudocode examples and brief explanations.

Operator | Code | Explanation
------------ | ------------- | -------------
!|if( !a){ //do code}|This will execute only if A is not true
or|if (a or b){	//do code}|This will execute as long as ONE of the elements is TRUE
&&|if (a&&b){//do code}|This will execute ONLY if BOTH a and b are TRUE
XOR|public static boolean logicalXOR(boolean x, boolean y) { return ( ( x or y ) && ! ( x && y ) ); }|This will only execute if the truth values don’t match.

The examples above are all conditional boolean operators.  Java also has bitwise boolean operators with similar properties.  

## Bitwise Negation Truth Table

| a 	| ~a 	|
|---	|----	|
| 1 	| 0  	|
| 0 	| 1  	|

## Bitwise Or, And, and Exclusive Or Truth Table


<style type="text/css">
	table.tableizer-table {
		font-size: 12px;
		border: 1px solid #CCC; 
		font-family: Verdana, Geneva, sans-serif;
	} 
	.tableizer-table td {
		padding: 4px;
		margin: 3px;
		border: 1px solid #CCC;
	}
	.tableizer-table th {
		background-color: #67138B; 
		color: #FFF;
		font-weight: bold;
	}
</style>
<table class="tableizer-table">
<thead><tr class="tableizer-firstrow"><th>a</th><th>b</th><th>a|b </th><th>a&b</th><th>a^b</th></tr></thead><tbody>
 <tr><td>0</td><td>1</td><td>1</td><td>0</td><td>1</td></tr>
 <tr><td>1</td><td>1</td><td>1</td><td>1</td><td>0</td></tr>
 <tr><td>0</td><td>0</td><td>0</td><td>0</td><td>0</td></tr>
 <tr><td>1</td><td>0</td><td>1</td><td>0</td><td>1</td></tr>
</tbody></table>

## Be careful!

When using boolean operators in Java, you have to be careful. There are fundamental differences between “&” and “&&”  and “|” and “||”. The single & and | REQUIRE the compiler to look at both conditions.  In contrast, as soon as the compiler sees that && and || has reached inevitability, it stops comparing and doesn’t validate the rest of the statement is true. 

## Keep Looking

You may have noticed that, despite the title of this post, you only spotted 8 boolean logical operators. What are the other 8 operators you ask?  Despite consulting with multiple expert programmers, the author was unable to identify the additional 8 rumored to be used in programming.  There was some speculation among the experts polled that comparison statements like !=, <, >, <=, >=, could be considered conditional boolean expressions.  In the search for the elusive 8 operators, even = and == were considered. However, no consensus could be reached in the time allotted since the expert programmers had to go to bed early. One can hope that, in the future, exciting new research will merit follow up post detailing the mysterious additional boolean operators.
